from golang:1.18.2-alpine3.16
workdir /authapp
copy . .
ENV GO111MODULE=on
RUN go mod init github.com/bortizf/microservice-app-example/tree/master/auth-api && \
    go mod tidy && \
    go build

FROM alpine:3.16
WORKDIR /app
COPY --from=0 /authapp/auth-api /app/app
CMD [ "/app/app" ]