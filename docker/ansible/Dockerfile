FROM ubuntu:14.04
MAINTAINER Matthew Forrester

RUN useradd -m -s /bin/bash ubuntu
RUN echo "ubuntu ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers.d/10-ubuntu_no_password

# Update System
RUN DEBIAN_FRONTEND=noninteractive apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y upgrade

# Install Ansible
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install libssl1.0.0
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install python-dev
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install python-pip
RUN pip install ansible
RUN mkdir -p /etc/ansible
