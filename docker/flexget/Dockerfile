FROM python:alpine


# Create a user to run the application
WORKDIR  /root/flexget/

## Data and config volumes
#VOLUME   /home/flexget/.flexget
#VOLUME   /home/flexget/torrents

# Install build dependencies and FlexGet
RUN      apk add --no-cache --virtual  .build-deps gcc musl-dev && \
         pip3 install -U pip && pip3 install flexget transmissionrpc && \
         apk del .build-deps gcc musl-dev

# Add start script
COPY     start.sh /root/flexget/
RUN      chmod +x ./start.sh

CMD      ["./start.sh"]