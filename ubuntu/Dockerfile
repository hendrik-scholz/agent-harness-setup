FROM ubuntu:noble

RUN apt-get update && \
    apt-get install -y --no-install-recommends curl ca-certificates gnupg && \
    curl -fsSL https://deb.nodesource.com/setup_24.x | bash - && \
    apt-get install -y --no-install-recommends nodejs && \
    npm install -g --ignore-scripts @earendil-works/pi-coding-agent@1.1.0 && \
    apt-get purge -y curl gnupg && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN adduser --disabled-password --home /home/pi pi
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

CMD ["/bin/bash"]
