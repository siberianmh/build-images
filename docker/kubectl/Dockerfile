FROM alpine:3

ARG GIT_COMMIT

# https://github.com/kubernetes/kubernetes/releases
ENV KUBE_LASTEST_VERSION="v1.21.0"

RUN apk add --no-cache ca-certificates bash git openssh curl \
    && wget -q https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl -O /usr/local/bin/kubectl \
    && chmod +x /usr/local/bin/kubectl \
    && chmod g+rwx /root \
    && mkdir /config \
    && chmod g+rwx /config

WORKDIR /workdir

CMD bash
