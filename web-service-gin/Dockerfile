FROM golang:alpine AS builder 

WORKDIR /build 

ADD go.mod . 

COPY . .

RUN go build -o web-service-gin .

FROM alpine

WORKDIR /build

COPY --from=builder /build/web-service-gin /build/web-service-gin

CMD ["./web-service-gin"]
