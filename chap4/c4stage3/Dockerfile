from golang:1.13.4-alpine3.10 as builder
WORKDIR /src
COPY ./main.go /src
RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -a -installsuffix cgo -o startapp main.go

FROM scratch
COPY --from=builder ./src/startapp /startapp
CMD ["/startapp"]
