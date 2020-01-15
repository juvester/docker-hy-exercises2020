FROM ubuntu

RUN apt-get update && apt-get -y install curl git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker.git
WORKDIR /frontend-example-docker
RUN npm install
RUN npm run build
RUN npm install -g serve

EXPOSE 5000
CMD serve -s -l 5000 dist
