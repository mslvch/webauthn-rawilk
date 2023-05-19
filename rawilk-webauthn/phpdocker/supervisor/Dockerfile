FROM falcon4ik007/php8.1-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install supervisor
RUN apt-get update \
    && apt-get -y install supervisor \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

CMD /usr/bin/supervisord -n
