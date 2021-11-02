FROM alpine:latest

LABEL maintainer="Nima Bahramzadeh<nima.bahramzadeh@avasecurity.com"

# Installing chrony package
RUN apk add --no-cache chrony

# Copying chrony config into the folder
COPY chrony.conf /etc/chrony/chrony.conf

# Exposing NTP port UDP 123
EXPOSE 123/udp

# start chronyd in the foreground
ENTRYPOINT [ "chronyd", "-d", "-x", "-L", "0", "-u", "chrony" ]
