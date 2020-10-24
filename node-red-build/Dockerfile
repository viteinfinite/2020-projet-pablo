FROM nodered/node-red
COPY package.json .
USER root
RUN apk add alsa-utils alsa-utils-doc alsa-lib alsaconf
USER node-red
RUN npm install --unsafe-perm --no-update-notifier --no-fund --only=production
