FROM forbesmyester/ansible
MAINTAINER Matthew Forrester

ADD ansible /tmp/ansible-scripts/forbesmyester/node

# Install Node / NPM etc - Note would be done below anyway, this is for easier
# development of Dockerfile (an intermediate image)
WORKDIR /tmp/ansible-scripts/forbesmyester/node
RUN echo [node] > /etc/ansible/hosts
RUN echo 127.0.0.1 >> /etc/ansible/hosts
RUN sudo su ubuntu -c "ansible-playbook -c local main.yml"
