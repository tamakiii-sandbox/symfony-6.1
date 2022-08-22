FROM amazonlinux:2.0.20220719.0

RUN yum update -y && \
    yum install -y yum-utils

RUN amazon-linux-extras install -y epel && \
    yum-config-manager --enable epel && \
    yum install -y https://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    yum-config-manager --enable remi-php81

RUN yum update -y && \
    yum install -y \
      php81 \
      which \
      less \
      make

RUN alternatives --install /usr/bin/php php /usr/bin/php81 1
