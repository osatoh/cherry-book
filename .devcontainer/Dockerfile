FROM ruby:3.1.2

RUN gem install rufo

# Set locale as ja_JP.UTF-8
RUN apt-get update \
  && apt-get install -y locales \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
RUN sed -i -E 's/# (ja_JP.UTF-8)/\1/' /etc/locale.gen \
  && locale-gen
ENV LANG ja_JP.UTF-8