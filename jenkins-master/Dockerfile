FROM jenkins/jenkins:lts
USER root
RUN apt-get update && apt-get install python3 python3-pip virtualenv -y
USER jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
