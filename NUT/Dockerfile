FROM --platform=$TARGETPLATFORM alpine:latest

ENV UPS_NAME="ups"
ENV UPS_DESC="UPS"
ENV UPS_DRIVER="usbhid-ups"
ENV UPS_PORT="auto"

ENV API_PASSWORD=""
ENV ADMIN_PASSWORD=""

RUN apk update
RUN apk add nut

RUN	install -d -m 750 -o nut -g nut /var/run/nut
	
COPY ./docker-entrypoint /usr/local/bin/
CMD ["docker-entrypoint"]