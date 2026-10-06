FROM golang:1.24-alpine

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o review-service .

EXPOSE 8081

CMD ["./review-service"]