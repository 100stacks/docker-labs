# 01-lab | docker build --no-cache -t alpine-demo -f Dockerfile .

FROM alpine:3.21.2

RUN apk update \
  && apk add --no-cache htop

COPY /src /src


CMD ["ls", "-al"]
