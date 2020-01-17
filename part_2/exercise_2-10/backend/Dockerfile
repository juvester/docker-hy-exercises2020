FROM ubuntu

RUN apt-get update && apt-get -y install curl git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs

RUN git clone https://github.com/docker-hy/backend-example-docker.git
WORKDIR /backend-example-docker
RUN npm install

EXPOSE 8000
ENV FRONT_URL=http://localhost:5000
CMD npm start
