FROM centos:centos7
LABEL maintainer="kevintham91@gmail.com"

RUN yum -y install socat && \
	yum clean all

VOLUME /var/run/docker.sock

# docker tcp port
EXPOSE 2375

ENTRYPOINT ["socat", "TCP-LISTEN:2375,reuseaddr,fork", "UNIX-CLIENT:/var/run/docker.sock"]

