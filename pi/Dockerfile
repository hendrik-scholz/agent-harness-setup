FROM alpine:3.24.2

RUN apk add --no-cache nodejs npm tzdata && \
    npm install -g --ignore-scripts @earendil-works/pi-coding-agent@1.4.0 && \
    npm cache clean --force

RUN adduser -h /home/pi -D pi
RUN addgroup pi pi
RUN mkdir -p /home/pi/.pi/agent

# additional tools
RUN apk add --no-cache git

# additional files
ADD mcp.json /home/pi/.pi/agent

RUN chown -R pi:pi /home/pi/.pi
USER pi

# Pi packages
RUN pi install git:github.com/hendrik-scholz/pi-today
RUN pi install npm:pi-context-view
RUN pi install npm:pi-llama-cpp

WORKDIR /home/pi

CMD ["/bin/sh"]