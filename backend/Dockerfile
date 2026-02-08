FROM golang:1.25-alpine

WORKDIR /backend

COPY go.mod go.sum* ./

RUN go mod download 

COPY . .

RUN go build -o /server ./cmd/app/main.go

CMD ["/server"]
