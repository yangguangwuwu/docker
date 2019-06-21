FROM php:7.2-cli-alpine3.9
MAINTAINER 15093565100@163.com
ADD swoole-4.3.5.tgz /tmp/
RUN echo http://mirrors.ustc.edu.cn/alpine/v3.9/main > /etc/apk/repositories && \
    echo http://mirrors.ustc.edu.cn/alpine/v3.9/community >> /etc/apk/repositories && \
    apk update && apk upgrade && apk add m4 autoconf make gcc g++ linux-headers && \
    cd /tmp/swoole-4.3.5 && phpize && ./configure && make && make install && \
    docker-php-ext-install pdo_mysql && docker-php-ext-enable swoole && rm -rf /tmp/*
CMD ["php","-m"]