FROM alpine:3.7

RUN apk add --no-cache 'su-exec>=0.2'
RUN apk add --no-cache haproxy

COPY haproxy.cfg /etc/haproxy/haproxy.cfg

EXPOSE 80 8181

COPY docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["haproxy", "-f", "/usr/local/etc/haproxy/haproxy.cfg"]