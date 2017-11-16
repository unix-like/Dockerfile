FROM ubuntu

MAINTAINER xiao xing <root@unix-like.com>

RUN apt-get update && apt-get install -y \
    openssh-server \
 && mkdir /var/run/sshd \
 && echo 'root:root' |chpasswd \
 && sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config \
 && sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config \
 && mkdir /root/.ssh \
 && echo 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDL1cGftYcwBml+2Kfhn0q62lsLvULzpK1oO6g6xzh96WZHCY1i2PBiFnC0v7kXUI02cSKP/QmJ9XVdIlLgWOveDpvwAT+niCgf8K1edLgcApQ7qVWK9wzjQfVnk+evQZBW4yT5bLX9ydHVJGwp2JJjiUP60Zc5dxf9g5hWMFUCOYGl4kut00ebRo1HfvPUTFvLZSBXFwCilLV1CIdRBs3JMJ8KWMecAvRmLSkY9WRK51Ci9EJQRYfrc1MZR/fdb8FXZ4vPc3dFA0TTGxB6cX60Lig+rhFOsm8Sdw70dawziP1vGOwWYBlPFW5erMHBei/+LjPhnh0s3Nq9fYvmovav xiaoxing@unix-like.local' > /root/.ssh/authorized_keys \
 && ln -s /usr/bin/python3.5 /bin/python \
 && rm -rf /var/lib/apt/lists/* \
 && rm -rf /var/cache/apt/archives/*

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
