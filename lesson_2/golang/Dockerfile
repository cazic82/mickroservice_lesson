FROM golang:1.16-alpine

WORKDIR /app/golang

ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/golang/go.mod ./

ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/golang/go.sum ./

RUN go mod download

ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/golang/main.go ./

ENTRYPOINT go run /app/golang -addr="0.0.0.0:8080"