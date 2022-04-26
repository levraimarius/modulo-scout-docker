FROM php:8.1-fpm-buster

RUN docker-php-ext-install pdo pdo_mysql && \
	docker-php-ext-enable pdo pdo_mysql && \
	apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git && \
	apt-get install -y yarn && \
	apt-get install curl && \
	curl -sL https://deb.nodesource.com/setup_14.x | bash && \
	apt-get install nodejs && \
	npm install && \
	npm add --also=dev @symfony/webpack-encore

COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

