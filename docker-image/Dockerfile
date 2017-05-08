FROM fluent/fluent-bit:0.11.4
MAINTAINER Eduardo Silva <eduardo@treasure-data.com>
USER root

COPY fluent-bit.conf /fluent-bit/etc/
COPY parsers.conf /fluent-bit/etc/

RUN mkdir /data

ADD https://github.com/oklog/oklog/releases/download/v0.2.1/oklog-0.2.1-linux-amd64 /oklog
RUN ["chmod", "775", "/oklog"]

CMD ["/fluent-bit/bin/fluent-bit", "-c", "/fluent-bit/etc/fluent-bit.conf"]
