FROM php:7-fpm-alpine


RUN echo "@testing http://nl.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories && \
    echo "@community http://nl.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories && \
    apk --update add \
        php7-xdebug@testing \
        php7-intl@community \
    && rm -rf /var/cache/apk/* \
    && cp /usr/lib/php7/modules/* /usr/local/lib/php/extensions/no-debug-non-zts-20151012/ \

#RUN pecl install xdebug


