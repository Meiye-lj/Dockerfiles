FROM ruby:2.7
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /sidekiq
RUN git clone https://github.com/sidekiq/sidekiq.git .
RUN git checkout v7.2.1
RUN gem install sqlite3 -v '1.4.2' && \
gem install bundler -v '2.2.28' && \
bundle add sidekiq
CMD ["/bin/bash"]