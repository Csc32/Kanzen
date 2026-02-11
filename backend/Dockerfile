FROM golang:1.25-alpine

WORKDIR /backend
#install Air for hot-realoading

RUN go install github.com/air-verse/air@latest

COPY go.mod go.sum* ./

RUN go mod download 
COPY . .

CMD ["air", "--build.cmd","go build -o cmd/app/main cmd/app/main.go", "--build.bin","./cmd/app/main"]
