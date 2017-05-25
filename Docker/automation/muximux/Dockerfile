############################################################
# docker build -t <dockername>/muximux .
# docker run --name muximux_00 -p 8080:3000 -id <dockername>/muximux
############################################################

FROM ioft/armhf-ubuntu

WORKDIR /opt

RUN apt-get update
RUN apt-get install -y git-core npm
RUN update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10
RUN git clone https://github.com/onedr0p/manage-this-node
WORKDIR /opt/manage-this-node
RUN npm install
COPY config.json.template /opt/manage-this-node/config.json
COPY Mountain /etc/localtime

EXPOSE 3000
ENTRYPOINT npm start && /bin/bash
