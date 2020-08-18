FROM ruby:2.6.0

RUN git clone https://github.com/docker-hy/rails-example-project.git /mydir

WORKDIR /mydir

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN gem install bundler && bundle install && rails db:migrate

CMD ["rails", "s"]