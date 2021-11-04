FROM alpine:3.12.2

LABEL maintainer=aanogueira
LABEL contact=aanogueira@protonmail.com

# Install postfix and supervisor
RUN apk add --no-cache \
    postfix \
    rsyslog \
	libsasl \
	cyrus-sasl-plain \
	cyrus-sasl-login \
    supervisor && \
    /usr/bin/newaliases

# Copy files into container
COPY . /

# SMTP port
EXPOSE 25

ENTRYPOINT [ "/entrypoint.sh" ]
