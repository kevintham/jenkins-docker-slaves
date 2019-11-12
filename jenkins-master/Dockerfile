FROM jenkins/jenkins:2.203
LABEL maintainer="kevintham91@gmail.com"

USER root
RUN mkdir /var/log/jenkins
RUN mkdir /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins
RUN chown -R jenkins:jenkins /var/cache/jenkins
USER jenkins

ENV JAVA_OPTS="-Xmx2048m"
ENV JENKINS_OPTS=" --handlerCountMax=20 --logfile=/var/log/jenkins/jenkins.log --webroot=/var/cache/jenkins/war"

