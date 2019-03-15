FROM node10.14:alpine

ARG project_dir=/app/
COPY . ${project_dir}
WORKDIR ${project_dir}

RUN set -x && \
    apk add --update --no-cache git \
                                vim && \
    npm install -g cordova \
                   ionic \
                   grunt-cli \
                   gulp \
                   bower && \
    npm install

EXPOSE 8100 35729

CMD ["ionic", "serve"]
# CMD ["ionic", "serve", "--all", "--port", "8100", "--livereload-port", "35729"]
