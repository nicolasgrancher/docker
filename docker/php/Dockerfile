FROM php:7-fpm-alpine

ENV TZ=Europe/Paris

RUN rm -rf /var/cache/apk/* && \
    rm -rf /tmp/* && \
	apk update && \
	
	apk add tzdata && \
	cp /usr/share/zoneinfo/$TZ /etc/localtime && \
	echo $TZ > /etc/timezone && \
	apk del tzdata && \
	
	apk add bash && \
	rm -rf /var/cache/apk/*

COPY php.ini /usr/local/etc/php/
