FROM ubuntu:16.04

# Install packages for building ruby
RUN apt update
RUN apt install -y build-essential curl git zlib1g-dev libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt-dev libsqlite3-dev nodejs tzdata
RUN apt clean

# Install rbenv and ruby-build
RUN git clone https://github.com/rbenv/rbenv.git /root/.rbenv
RUN git clone https://github.com/rbenv/ruby-build.git /root/.rbenv/plugins/ruby-build
RUN /root/.rbenv/plugins/ruby-build/install.sh

ENV PATH /root/.rbenv/bin:$PATH

RUN echo 'eval "$(rbenv init -)"' >> /etc/profile.d/rbenv.sh
RUN echo 'eval "$(rbenv init -)"' >> /root/.bashrc

# Install version 2.6.0 of ruby
RUN rbenv install 2.6.0
RUN rbenv global 2.6.0

ENV PATH /root/.rbenv/shims/:$PATH

RUN echo 'gem: --no-rdoc --no-ri' >> /root/.gemrc
RUN gem environment --config-file /root/.gemrc

# Copy files
WORKDIR /src/app

COPY . ./

# Install gems
ENV BUNDLE_SILENCE_ROOT_WARNING 1

RUN gem install bundler
RUN bundle install
RUN rbenv rehash

# Rails
RUN rails db:migrate

EXPOSE 3000

CMD ["rails", "s"]
