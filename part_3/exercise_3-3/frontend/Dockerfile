FROM ubuntu:16.04

RUN apt-get update && apt-get -y install curl git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get -y install nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /app && \
    cd /app && npm install && \
    apt-get purge -y --auto-remove curl git && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /app

USER app

WORKDIR /app

CMD npm start
