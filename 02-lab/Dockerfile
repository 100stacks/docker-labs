# 02-lab | docker build --no-cache -t second-demo-alpine -f Dockerfile .
# docker image ls second-demo-alpine

FROM alpine

RUN apk update \
  && apk add --no-cache htop

COPY /src /src

CMD ["ls", "-al"]

RUN ls
