FROM nodered/node-red
COPY package.json .
USER root
ENV PYTHONUNBUFFERED=1
RUN apk add alsa-utils alsa-utils-doc alsa-lib alsaconf
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools
RUN apk add python3-dev
RUN pip3 install spidev gpiozero numpy
USER node-red
RUN npm install --unsafe-perm --no-update-notifier --no-fund --only=production
