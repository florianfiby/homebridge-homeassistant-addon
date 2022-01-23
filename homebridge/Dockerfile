ARG BUILD_FROM
FROM $BUILD_FROM

# Add env
ENV LANG C.UTF-8

# Setup base
RUN apk add --no-cache jq
RUN apk add nodejs 
RUN apk add npm

# Setup Homebridge
RUN npm install -g --unsafe-perm homebridge
RUN npm install -g --unsafe-perm homebridge-config-ui-x
RUN npm install -g --unsafe-perm homebridge-ring
RUN npm install -g --unsafe-perm homebridge-alexa
RUN npm install -g --unsafe-perm homebridge-homeassistant-saaak

# Copy root filesystem
COPY rootfs /

EXPOSE 8581
EXPOSE 51856

CMD [ "homebridge" ]
