FROM ubuntu:xenial
MAINTAINER Alejandro Guirao <lekumberri@gmail.com>

RUN apt-get update && apt-get -y install ruby ruby-dev build-essential zlib1g-dev
RUN gem install --no-ri --no-rdoc riemann-tools
