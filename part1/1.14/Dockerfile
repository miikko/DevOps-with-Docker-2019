FROM ruby:2.6.0

RUN bundle config --global frozen 1
WORKDIR /ruby-example
COPY Gemfile Gemfile.lock ./
RUN bundle install
# Project should be pulled and placed in the same directory with this Dockerfile
COPY . .
RUN apt-get update && apt-get install -y nodejs
RUN rails db:migrate

CMD rails s