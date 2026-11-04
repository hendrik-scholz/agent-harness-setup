FROM python:3.14.10-alpine3.24

RUN pip install --upgrade pip && \
    pip install mistral-vibe==2.25.0 # https://github.com/mistralai/mistral-vibe/issues/1194

RUN adduser -h /home/vibe -D vibe
RUN addgroup vibe vibe
RUN mkdir -p /home/vibe/.vibe

# additional tools
RUN apk add --no-cache git

# additional files
ADD config.toml /home/vibe/.vibe

RUN chown -R vibe:vibe /home/vibe/.vibe
USER vibe

WORKDIR /home/vibe

CMD ["/bin/sh"]