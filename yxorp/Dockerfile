FROM alpine:latest
RUN apk add --no-cache netcat-openbsd
RUN mkfifo reply
EXPOSE 1234
CMD nc -kl 1234 < reply | nc 127.0.0.1 31337 > reply
