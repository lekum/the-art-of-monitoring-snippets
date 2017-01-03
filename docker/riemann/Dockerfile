FROM java:8
MAINTAINER Alejandro Guirao <lekumberri@gmail.com>

ENV RIEMANN_VERSION 0.2.11

RUN apt update && apt install -y mailutils
RUN wget -O /tmp/riemann_${RIEMANN_VERSION}_all.deb https://aphyr.com/riemann/riemann_${RIEMANN_VERSION}_all.deb -P /tmp/
RUN echo "8f074b9ad3321a962d3a32a7a54cf930 /tmp/riemann_${RIEMANN_VERSION}_all.deb" \
    > /tmp/riemann_${RIEMANN_VERSION}.md5 && \
    md5sum -c /tmp/riemann_${RIEMANN_VERSION}.md5 && \
    dpkg -i /tmp/riemann_${RIEMANN_VERSION}_all.deb && \
    rm /tmp/riemann* && \
    mkdir -p /etc/riemann/conf.d
COPY riemann.config /etc/riemann/
COPY email.clj /etc/riemann/examplecom/etc/
EXPOSE 5555 5556
ENTRYPOINT ["/usr/bin/riemann"]
CMD ["start"]
