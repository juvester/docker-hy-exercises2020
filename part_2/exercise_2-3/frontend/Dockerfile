FROM ubuntu

RUN apt-get update && apt-get -y install curl git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker.git
WORKDIR /frontend-example-docker
RUN npm install

EXPOSE 5000
ENV API_URL=http://localhost:8000
CMD npm start
