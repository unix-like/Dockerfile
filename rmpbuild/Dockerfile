FROM centos:6.9

RUN yum install -y \
    rpmdevtools.noarch \
    rpm-build \
    epel-release.noarch \
    gcc \
    pcre-devel \
    openssl-devel \
    vim \
    libxml2-devel \
 && /usr/sbin/useradd makerpm \
 && /usr/sbin/groupadd mock \
 && usermod -a -G mock makerpm \
 && echo "301415926" | passwd --stdin makerpm \
 && mkdir /home/makerpm/rpmbuild \
 && chown makerpm:makerpm /home/makerpm/rpmbuild
