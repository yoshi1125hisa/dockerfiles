FROM node:16.3.0-alpine

ARG project_dir=/app/

COPY . ${project_dir}
WORKDIR ${project_dir}

RUN set -x && \
    apk upgrade --no-cache && \
    apk add --update --no-cache git && \
    npm install -g npm@6.4.1 && \
    npm install

EXPOSE 8000 

CMD ["env", "PORT=8000", "npm", "start"]
