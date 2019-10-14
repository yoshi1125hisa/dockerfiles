FROM swift:4.0.3

# USER root

ARG project_dir=/server

RUN set -x && \
    mkdir -p ${project_dir}

COPY ./Config /server/Config
COPY ./Sources /server/Sources
COPY ./Makefile /server/Makefile
COPY ./Package.resolved /server/Package.resolved
COPY ./Package.swift /server/Package.swift

ENV PORT 9000
EXPOSE $PORT

WORKDIR ${project_dir}

RUN set -x && \
    make build

CMD ["make", "run"]
