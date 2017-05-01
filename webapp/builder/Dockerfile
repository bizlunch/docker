FROM phusion/baseimage:0.9.21

RUN apt-get update && apt-get install -y curl git

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash - && \
     apt-get install -y nodejs

RUN npm install -g bower gulp --silent

RUN useradd --uid 999 --create-home gitlab-runner
