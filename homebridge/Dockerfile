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

CMD [ "homebridge" ]
