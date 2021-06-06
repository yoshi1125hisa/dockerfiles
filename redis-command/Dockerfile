FROM node:16.3.0-alpine

RUN set -x && \
    npm install -g redis-commander

ENTRYPOINT ["redis-commander"]

EXPOSE 8080

CMD [ "--redis-host", "redis", "--port", "8080" ]
