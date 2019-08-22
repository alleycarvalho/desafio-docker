FROM nginx:1.17.0-alpine

LABEL maintainer="Alley M. Carvalho <alleycarvalho@gmail.com>"

#####################################################################
# RUN Setup:
#####################################################################

RUN apk update && apk upgrade \
    # Install dependencies, softwares, etc.
    && apk add --no-cache \
    openssl \
    # Remove cache
    && rm -rf /tmp/* /var/cache/apk/* \
    # Remove html
    && rm -rf /var/www/html

RUN rm /etc/nginx/conf.d/default.conf

# Install dockerize
ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

# Set default work directory
WORKDIR /var/www
