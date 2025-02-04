# `FROM` Command ... implies "ancestry"

= **Has** to be the first executable command (not a comment `#`)

```
docker-labs/04-lab on  origin/init-docker-labs [⇡!] on 🐳 vdev via 🅒 spark
➜ docker build -t demo-jenkins -f Dockerfile .
[+] Building 1.1s (5/5) FINISHED                                                                                                                docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                            0.0s
 => => transferring dockerfile: 367B                                                                                                                            0.0s
 => [internal] load metadata for docker.io/jenkins/jenkins:lts-jdk11                                                                                            1.6s
 => [internal] load .dockerignore                                                                                                                               0.0s
 => => transferring context: 2B                                                                                                                                 0.0s
 => CACHED [1/2] FROM docker.io/jenkins/jenkins:lts-jdk11@sha256:6aa6c6bd7da914bf5333305c8102cb26965ea4b227e37f4269315725a2b0cd81                               0.0s
 => => resolve docker.io/jenkins/jenkins:lts-jdk11@sha256:6aa6c6bd7da914bf5333305c8102cb26965ea4b227e37f4269315725a2b0cd81                                      0.0s
 => ERROR [2/2] RUN apt-get update && apt-install git                                                                                                           0.2s
------
 > [2/2] RUN apt-get update && apt-install git:
0.211 Reading package lists...
0.218 E: List directory /var/lib/apt/lists/partial is missing. - Acquire (13: Permission denied)
------
Dockerfile:7
--------------------
   5 |     FROM jenkins/jenkins:lts-jdk11
   6 |
   7 | >>> RUN apt-get update && apt-install git
   8 |
   9 |
--------------------
ERROR: failed to solve: process "/bin/sh -c apt-get update && apt-install git" did not complete successfully: exit code: 100
```


