FROM ubuntu:xenial
MAINTAINER Alejandro Guirao <lekumberri@gmail.com>

RUN apt-get update && apt-get -y install curl
RUN curl https://packagecloud.io/gpg.key | apt-key add -
RUN echo deb https://packagecloud.io/exoscale/community/ubuntu/ xenial main > /etc/apt/sources.list.d/exoscale_community.list
RUN echo deb https://packagecloud.io/grafana/stable/debian/ wheezy main > /etc/apt/sources.list.d/packagecloud_grafana.list
ENV UPDATED_AT 2017_01_12_15_00
RUN apt-get update
RUN apt-get -yq install graphite-carbon apt-transport-https graphite-api
