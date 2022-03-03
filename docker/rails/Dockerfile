FROM ruby:2.7.5

#####################################
# Install Packages
#####################################
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
        && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
        && apt-get update -qq \
        && apt-get install -y build-essential libpq-dev nodejs yarn

#####################################
# Create workspace
#####################################
RUN mkdir /src
WORKDIR /src

#####################################
# Restore ruby packages
#####################################
COPY ./Gemfile /src/Gemfile
COPY ./Gemfile.lock /src/Gemfile.lock
RUN bundle install

#####################################
# entrypoint
#####################################
COPY ./docker/rails/entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
EXPOSE 3000
