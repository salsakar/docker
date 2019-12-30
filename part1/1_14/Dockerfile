FROM ruby:2.6.0

WORKDIR /app
COPY . /app

RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs

RUN gem install bundler
RUN bundle install

ENV RAILS_ENV=production
ENV SECRET_KEY_BASE secret

RUN rake assets:precompile
RUN rails db:migrate
RUN rake assets:precompile

EXPOSE 3000
CMD ["rails", "s", "-e"]
