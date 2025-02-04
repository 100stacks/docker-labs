# demo showing NON-ROOT user - "jenkins"
# $ docker container run --rm -it jenkins/jenkins:lts-jdk11 bash  (works from cli)
# $ docker build -t demo-jenkins Dockerfile . (DOES NOT WORK - permisson issue since NOT root)

FROM jenkins/jenkins:lts-jdk11

RUN apt-get update && apt-install git

