FROM golang:1-alpine3.18

WORKDIR /go/src/hotapp
COPY *.go .

RUN apk update \
    && apk add --no-cache git \
    && go get -d ./... \
    && apk del git

RUN go install ./...

CMD ["hotapp"]
