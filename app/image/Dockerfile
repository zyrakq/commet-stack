FROM alpine:latest AS builder
ARG RELEASE
RUN apk add --no-cache wget

WORKDIR /tmp
RUN wget https://github.com/commetchat/commet/releases/download/${RELEASE}/commet-web.tar.gz
RUN tar -xzvf ./commet-web.tar.gz
RUN mv web /app

FROM docker.io/nginx:alpine
RUN rm -rf /usr/share/nginx/html
COPY --from=builder /app /usr/share/nginx/html