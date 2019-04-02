FROM php:7.2

RUN apt-get update -yqq
RUN apt-get install apt-utils -y
RUN apt-get install git -yqq
RUN apt-get install -y zlib1g-dev libfreetype6-dev libjpeg62-turbo-dev libpng12-dev libxpm-dev libvpx-dev libmcrypt-dev libgmp-dev
RUN apt-get install wget -y

RUN docker-php-ext-configure gd \
     --with-freetype-dir=/usr/lib/x86_64-linux-gnu/ \
     --with-jpeg-dir=/usr/lib/x86_64-linux-gnu/ \ 
     --with-xpm-dir=/usr/lib/x86_64-linux-gnu/  \
     --with-vpx-dir=/usr/lib/x86_64-linux-gnu/ 

RUN docker-php-ext-install pdo pdo_mysql mysqli opcache zip gd

RUN curl -sS https://getcomposer.org/installer| php





