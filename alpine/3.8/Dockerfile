FROM alpine:3.8
LABEL maintainer="Miguel A. Pari Rojas"

ENV ROOT_PASSWORD=root

RUN apk update
RUN apk add openssh
RUN echo "root:${ROOT_PASSWORD}" | chpasswd

EXPOSE 22

CMD [ "sh" ]