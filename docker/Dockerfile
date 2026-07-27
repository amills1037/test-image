FROM debian:trixie

## Update packages to install
RUN apt-get update

RUN apt-get install -y openssh-server

RUN apt-get install -y sudo

RUN useradd -m -s /bin/bash dev
## we are going to update
# RUN mkdir /home/dev/.ssh
# RUN chmod 700 /home/dev/.ssh

RUN echo "dev ALL=(ALL) NOPASSWD:ALL\n" >/etc/sudoers.d/99-dev-user

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
