FROM centos:latest
MAINTAINER Juan Manuel Rey "juanmanuel.reyportal@gmai.com"
RUN yum install -y https://repos.fedorapeople.org/repos/openstack/openstack-mitaka/rdo-release-mitaka-5.noarch.rpm
RUN yum update -y
RUN yum install -y openstack-rally \
                openstack-utils \
                openstack-selinux \
                gcc \
                libffi-devel \
                python-devel \
                openssl-devel \
                gmp-devel \
                libxml2-devel \
                libxslt-devel \
                postgresql-devel \
                redhat-rpm-config \
                wget \
                which

VOLUME ["/home/rally"]
WORKDIR /home/rally

CMD ["bash", "--login"]
RUN rally-manage db create
