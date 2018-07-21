FROM alpine:3.8
LABEL maintainer="Miguel A. Pari Rojas"

RUN apk update
RUN apk add openssh
RUN echo "root:root" | chpasswd

EXPOSE 22

CMD [ "sh" ]