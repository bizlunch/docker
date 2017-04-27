FROM phusion/baseimage:0.9.21

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
	apt-get install -y \
	                curl unzip \
					php php-curl php-zip php-pdo php-gd php-xml php-apcu php-mysql php-intl \
					nginx-light
          
RUN mkdir /etc/service/nginx

ADD services/nginx      /etc/service/nginx/run

ADD misc/init       /etc/my_init.d/00_my_init

RUN rm -rf /etc/service/{sshd,syslog-forwarder,syslog-ng} && \
    rm -rf /etc/my_init.d/00_regen_ssh_host_keys.sh

EXPOSE 80

RUN rm -rf /var/lib/apt/lists/*

ENV STAGE_ENV=prod

WORKDIR /var/www
