FROM golang:1.21-alpine AS builder
WORKDIR /app
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN go build -o http-server-projeto-korp .

FROM alpine:latest
RUN apk --no-cache add ca-certificates
WORKDIR /root/
COPY --from=builder /app/http-server-projeto-korp .
EXPOSE 8080
CMD ["./http-server-projeto-korp"]
