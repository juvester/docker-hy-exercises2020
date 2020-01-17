FROM node:10-alpine3.11 as build-stage
RUN apk add --no-cache curl git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /app && \
    cd /app && npm install && \
    apk del curl git && \
    adduser -D app && \
    chown -R app /app
USER app
WORKDIR /app
RUN npm run build

FROM node:10-alpine3.11
COPY --from=build-stage /app/dist/ /app/dist
WORKDIR /app
RUN npm install -g serve
CMD serve -s -l 5000 dist
