FROM ubuntu:16.04
LABEL maintainer="ppichier@student.le-101.fr"
LABEL description="Gitlab Dockerfile"

RUN apt-get -y update
RUN apt-get install -y dialog apt-utils
RUN apt-get install -y curl openssh-server ca-certificates git
#RUN apt-get install -y postfix
RUN curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash
RUN apt-get install -y gitlab-ce
#RUN gitlab-ctl reconfigure

EXPOSE 80 443 22 
