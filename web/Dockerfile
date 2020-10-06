# BUILD
FROM golang:1.9.1-alpine3.6 as builder

# WORKDIR /Users/sandeep.vuzzini/codefreshtest/

COPY dispatcher.go .
RUN go build dispatcher.go

# RUN
FROM alpine:edge

EXPOSE 80
CMD ["/dispatcher"]

COPY --from=builder /go/dispatcher /
COPY static /Users/sandeep.vuzzini/Dropbox/Algorithms/k8s-wordsmith-demo
