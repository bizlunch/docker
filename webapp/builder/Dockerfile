FROM phusion/baseimage:0.9.21

RUN apt-get update && apt-get install curl git

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash - && \
     apt-get install nodejs

RUN npm install -g bower gulp --silent
