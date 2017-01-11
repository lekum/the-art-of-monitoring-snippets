FROM ubuntu:xenial
MAINTAINER Alejandro Guirao <lekumberri@gmail.com>

ENV UPDATED_AT 2017_01_11_13_30
RUN apt-get update && apt-get -y install software-properties-common
RUN add-apt-repository ppa:collectd/collectd-5.5
RUN apt-get update && apt-get -y install collectd
COPY collectd.conf /etc/collectd/
ENTRYPOINT ["collectd"]
CMD ["-f"]
