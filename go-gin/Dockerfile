FROM golang:1.14-alpine

RUN set -x && \
    apk upgrade --no-cache && \
    go get -u github.com/gin-gonic/gin && \
    go get -u github.com/jinzhu/gorm && \
    go get github.com/pilu/fresh && \
    go get -u github.com/jinzhu/gorm/dialects/mysql

ARG project_dir=/go/src/<X>

COPY . ${project_dir}

WORKDIR ${project_dir}

ENV MYSQL_PRODUCTION_DB_HOST dummmy

EXPOSE 8080

# RUN adduser -D docker
# USER docker

CMD ["go", "run", "main.go"]
