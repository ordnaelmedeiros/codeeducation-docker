FROM golang:1.16.0-alpine3.12 as build
COPY ./rocks.go /go/rocks.go
RUN go build rocks.go

FROM scratch
COPY --from=build /go/rocks /app/rocks
CMD ["/app/rocks"]
