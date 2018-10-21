FROM debian
MAINTAINER Alex Krushinsky <akrushin@student.unit.ua>

EXPOSE 22 80 443
RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y wget ca-certificates openssh-server postfix vim
RUN apt install -y tzdata
RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && \
    chmod 777 script.deb.sh && \
    ./script.deb.sh && \
    apt-get install -y gitlab-ce
ENTRYPOINT /opt/gitlab/embedded/bin/runsvdir-start & gitlab-ctl reconfigure && watch -n 100 "cat /etc/fstab"

# docker build --tag=ex03 .
# docker run -it -p 8080:80 -p 8022:22 -p 8443:443 --rm ex03

# https://gitlab.com/gitlab-org/omnibus-gitlab/issues/430
# https://docs.gitlab.com/omnibus/docker/
# https://about.gitlab.com/installation/#debian