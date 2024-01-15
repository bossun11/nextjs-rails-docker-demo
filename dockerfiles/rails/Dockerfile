FROM ruby:3.2.0

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs cron

RUN mkdir /app
WORKDIR /app

COPY back/api/Gemfile /app/Gemfile
COPY back/api/Gemfile.lock /app/Gemfile.lock

RUN bundle install

COPY . /app