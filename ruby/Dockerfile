FROM ruby:2.3.0-slim

WORKDIR /app
COPY . /app/
RUN bundle install

EXPOSE 8080

CMD ["script/server"]
