FROM bizlunch/nginx

RUN  DEBIAN_FRONTEND=noninteractive apt-get update && \
	 DEBIAN_FRONTEND=noninteractive apt-get install -y \
					php php-curl php-zip php-pdo php-gd php-xml php-apcu php-mysql php-intl

ADD services/php        /etc/service/php/run

RUN chmod 600 /etc/cron.d/ktv && \
    chmod +x etc/service/php/run && \
    mkdir -p /opt/bizlunch/cache /var/lib/php/session && \
	  chown www-data:www-data -R /opt/bizlunch /var/lib/php/session && \
    rm -rf /var/lib/apt/lists/*
