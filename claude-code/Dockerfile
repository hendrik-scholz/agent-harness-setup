FROM alpine:3.24.4

RUN apk add --no-cache nodejs npm && \
    npm install -g @anthropic-ai/claude-code@2.1.319 && \
    npm cache clean --force

RUN adduser -h /home/claude -D claude
RUN addgroup claude claude

# additional tools
RUN apk add --no-cache git
RUN apk add --no-cache sox

# additional files

USER claude

WORKDIR /home/claude

CMD ["/bin/sh"]