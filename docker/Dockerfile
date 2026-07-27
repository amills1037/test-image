FROM debian:trixie

## Update packages to install
RUN apt-get update

## Install ssh server first.  Fingerprint is less likely to change if ssh server is installed first.
RUN apt-get install -y openssh-server

RUN useradd -m dev
RUN mkdir /home/dev/.ssh
RUN chmod 700 /home/dev/.ssh

RUN echo "dev ALL=(ALL) NOPASSWD:ALL\n" >/etc/sudoers.d/99-dev-user

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
