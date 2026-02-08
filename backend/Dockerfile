FROM golang:1.23.12-alpine

WORKDIR /backend

COPY go.mod go.sum ./

RUN go mod donwload 

COPY . .

RUN go build -v -o /usr/local/bin/app ./..

CMD ["app"]
