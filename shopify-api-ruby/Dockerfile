FROM ruby:2.7

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /shopify-api-ruby

RUN apt-get update && apt-get install -y \
build-essential \
libssl-dev \
libreadline-dev \
zlib1g-dev \
git \
&& git clone https://github.com/Shopify/shopify-api-ruby.git . \
&& git checkout v13.4.0 \
&& gem install bundler:2.2.3 \
&& bundle install

CMD ["/bin/bash"]