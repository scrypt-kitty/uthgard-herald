FROM ubuntu:14.04

RUN apt-get update

RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
RUN apt-get install -y nodejs

RUN apt-get install -y git
RUN cd /opt/ && git clone https://github.com/thekroko/uthgard-herald
RUN cd /opt/uthgard-herald/herald && npm install
RUN npm install -g angular
RUN npm install -g angular-cli

EXPOSE 4200

CMD cd /opt/uthgard-herald/herald | ng serve
