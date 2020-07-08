FROM alpine:3.12

MAINTAINER berosek <berosek@gmail.com>

# Install postfix and supervisor
RUN apk add --no-cache \
        postfix \
        rsyslog \
        supervisor && \
        /usr/bin/newaliases

# Copy files into container
COPY . /

# SMTP port
EXPOSE 25

ENTRYPOINT [ "/entrypoint.sh" ]
