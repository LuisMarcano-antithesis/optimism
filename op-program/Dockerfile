ARG OP_STACK_GO_BUILDER=us-docker.pkg.dev/oplabs-tools-artifacts/images/op_stack_go:latest
FROM $OP_STACK_GO_BUILDER as builder
# See "make golang-docker" and /ops/docker/op-stack-go

FROM alpine:3.18

COPY --from=builder /usr/local/bin/op-program /usr/local/bin/op-program

CMD ["op-program"]
