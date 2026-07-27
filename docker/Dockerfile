FROM debian:trixie

## Update packages to install
RUN apt-get update

## Install ssh server first.  Fingerprint is less likely to change if ssh server is installed first.
RUN apt-get install -y openssh-server

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
