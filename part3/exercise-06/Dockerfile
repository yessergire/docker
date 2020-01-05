FROM ubuntu:16.04

ENV PATH /root/.rbenv/bin:/root/.rbenv/shims/:$PATH

# Install packages for building ruby
RUN apt update && apt install -y \
        build-essential curl git zlib1g-dev libssl-dev libreadline-dev \
        libyaml-dev libxml2-dev libxslt-dev libsqlite3-dev nodejs tzdata && \
    rm -rf /var/lib/apt/lists/* && \
# Install rbenv and ruby-build
    git clone https://github.com/rbenv/rbenv.git /root/.rbenv && \
    git clone https://github.com/rbenv/ruby-build.git /root/.rbenv/plugins/ruby-build  && \
    /root/.rbenv/plugins/ruby-build/install.sh  && \
    echo 'eval "$(rbenv init -)"' >> /etc/profile.d/rbenv.sh && \
    echo 'eval "$(rbenv init -)"' >> /root/.bashrc && \
# Install version 2.6.0 of ruby
    rbenv install 2.6.0 && \
    rbenv global 2.6.0 && \
    echo 'gem: --no-rdoc --no-ri' >> /root/.gemrc && \
    gem environment --config-file /root/.gemrc

# Copy files
WORKDIR /src/app

COPY . ./

# Install gems
ENV BUNDLE_SILENCE_ROOT_WARNING 1
RUN gem install bundler && \
    bundle install && \
    rbenv rehash && \
# Rails
    rails db:migrate

EXPOSE 3000

CMD ["rails", "s"]
