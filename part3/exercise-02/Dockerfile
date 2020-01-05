FROM ubuntu:16.04

WORKDIR /app

ENV LC_ALL=C.UTF-8

# Install dependencies
RUN apt update && \
    apt-get install -y rtmpdump gcc wget curl libav-tools python-dev \
    python-setuptools python-crypto python-requests python-lxml \
    php7.0-cli php7.0-curl php7.0-mcrypt && \
    rm -rf /var/lib/apt/lists/*

# Download youtube-dl and yle-dl
RUN curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl && \
    curl -L https://github.com/aajanki/yle-dl/archive/2.37.tar.gz -o yle-dl.tar.gz && \
    tar xzf yle-dl.tar.gz && chmod a+x /usr/local/bin/youtube-dl

# Install yle-dl
RUN phpenmod mcrypt && cd yle-dl-2.37 && python setup.py install && cd .. && rm -rf yle-dl-2.37

ENTRYPOINT ["yle-dl"]
