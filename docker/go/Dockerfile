FROM golang:1.16-alpine

RUN apk update \
    && apk upgrade

RUN go get github.com/cespare/reflex
ENV CGO_ENABLED=0

WORKDIR /go/src/api

COPY ./server .

RUN go mod download