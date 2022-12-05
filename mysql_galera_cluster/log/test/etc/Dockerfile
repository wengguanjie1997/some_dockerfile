FROM alpine:3.16.2
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories &&\
cd /etc/apk/keys &&\
wget http://alpine.rsyslog.com//rsyslog@lists.adiscon.com-5a55e598.rsa.pub &&\
echo 'http://alpine.rsyslog.com//3.7/stable' >> /etc/apk/repositories &&\
apk add rsyslog tzdata --no-cache &&\
echo '#!/bin/sh' > /docker_entrypoint.sh && \
echo 'rm -fv /var/run/rsyslogd.pid' >> /docker_entrypoint.sh &&\
echo 'rsyslogd -n' >> /docker_entrypoint.sh
ENTRYPOINT [ "/bin/sh","/docker_entrypoint.sh" ]
