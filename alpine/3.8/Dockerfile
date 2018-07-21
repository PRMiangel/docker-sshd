FROM alpine:3.8
LABEL maintainer="Miguel A. Pari Rojas"

ENV ROOT_PASSWORD=root

RUN apk update
RUN apk add openssh
RUN mkdir /var/run/sshd
RUN echo "root:${ROOT_PASSWORD}" | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config

COPY entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/entrypoint.sh

EXPOSE 22

CMD ["/usr/local/bin/entrypoint.sh"]
