FROM node:10-alpine3.11

RUN apk add --no-cache curl git && \
    git clone https://github.com/docker-hy/backend-example-docker.git /app && \
    cd /app && npm install && \
    apk del curl git && \
    adduser -D app && \
    chown -R app /app

USER app

WORKDIR /app

CMD npm start
