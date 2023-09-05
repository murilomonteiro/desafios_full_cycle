FROM golang:alpine as builder

WORKDIR /usr/src/app

COPY . .

RUN go build -o /app HelloWorld.go

FROM scratch

COPY --from=builder /app /app

CMD ["/app"]