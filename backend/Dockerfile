FROM ruby:2.7.5

RUN apt-get update -qq && apt-get install -y build-essential nodejs

ADD https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh /wait-for-it.sh

RUN chmod +x /wait-for-it.sh

# Pre-install gems
WORKDIR /usr/src
COPY backend ./backend
WORKDIR /usr/src/backend
RUN bundle install
