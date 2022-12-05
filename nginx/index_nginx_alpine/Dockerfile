FROM alpine:3.16.2

RUN set -eux; \
        \
    sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories; \
    \
    apk add --no-cache \
    'nginx' \
    ; \
    \
    mkdir -p /data; \
    echo "Test nginx for alpine!" > /data/xxx.conf

COPY default.conf /etc/nginx/http.d/

EXPOSE 80

CMD ["nginx","-g","daemon off;"]

