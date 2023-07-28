FROM jenkins/jenkins:lts-jdk11

USER root
RUN curl -fsSL https://get.docker.com | sh
RUN apt-get update && apt-get install docker-compose-plugin
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

USER jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt