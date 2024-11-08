FROM golang:1.23 as build-env

WORKDIR /go/src/alert_generator
COPY . /go/src/alert_generator

ENV CGO_ENABLED 0

RUN go build ./cmd/alert_generator_compliance_tester

FROM quay.io/prometheus/busybox
COPY --from=build-env /go/src/alert_generator/alert_generator_compliance_tester /
COPY --from=build-env /go/src/alert_generator/rules.yaml /

ENTRYPOINT ["/alert_generator_compliance_tester"]
