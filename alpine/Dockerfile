FROM alpine:3.24.2

RUN apk add --no-cache nodejs npm && \
    npm install -g --ignore-scripts @earendil-works/pi-coding-agent@1.1.0 && \
    npm cache clean --force

RUN adduser -h /home/pi -D pi
RUN addgroup pi pi
RUN mkdir -p /home/pi/.pi/agent

# additional files
ADD mcp.json /home/pi/.pi

RUN chown -R pi:pi /home/pi/.pi
USER pi

# additional tools
# Pi packages
RUN pi install npm:pi-today
RUN pi install npm:pi-llama-cpp

WORKDIR /home/pi

CMD ["/bin/sh"]
