FROM ruby:2.6.3
RUN apt update && apt install -y postgresql-client nginx
RUN mkdir /app
WORKDIR /app
COPY Gemfile /Gemfile
COPY Gemfile.lock /Gemfile.lock
RUN bundle install
COPY . .
CMD ["rails", "server"]