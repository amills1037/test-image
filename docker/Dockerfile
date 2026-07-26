from debian:trixie

## Update packages to install
RUN apt update

## Install ssh server first.  Fingerprint is less likely to change if ssh server is installed first.
RUN apt install -y openssh-server
RUN service ssh start
