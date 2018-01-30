FROM vgbpowertech/ubuntu-16-apache-php-7.1-xdebug


# overwrite doc root for oro-web
ENV DOCUMENT_ROOT=html
ENV SMTP_RELAYHOST=mail:1025
ENV SMTP_HOSTNAME=mail
ENV SMTP_DOMAIN=

RUN apt-get update && apt-get install -y --allow-unauthenticated \
	mysql-client iputils-ping tree

# RUN /usr/local/bin/composer self-update
RUN chmod 777 /tmp -R

COPY docker /

RUN echo "setting PHP-options" && \
		phpenmod cust-opcache && \
		phpenmod cust-other && \
		phpenmod cust-xdebug && \
		echo "composer self-update" && \
		composer self-update && \
		service supervisor restart

WORKDIR /var/www/html
