FROM ruby:2.4.2-alpine

RUN set -x && \
    apk add --update --no-cache \
        postgresql-dev \
        nodejs \
        tzdata \
        libc-dev \
        libxml2-dev \
        build-base \
        curl-dev \
        libxslt-dev

ENV APP_PATH /app
ARG RAILS_ENV="development"

WORKDIR $APP_PATH

COPY Gemfile $APP_PATH
COPY Gemfile.lock $APP_PATH

RUN bundle install -j4 --with $RAILS_ENV

COPY . $APP_PATH

EXPOSE 3000

CMD ["bundle", "exec", "rake", "db:migrate"]
