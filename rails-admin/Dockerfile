FROM ruby:3.0
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /rails_admin
RUN git clone https://github.com/railsadminteam/rails_admin.git .
RUN git checkout v3.1.2
RUN apt-get update && \
apt-get install -y \
sqlite3 \
libsqlite3-dev \
default-libmysqlclient-dev \
libpq-dev \
nodejs
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - && \
apt-get install -y nodejs && \
npm install --global yarn
RUN bundle install
RUN yarn install
EXPOSE 3000
CMD ["rails", "s", "-b", "0.0.0.0"]