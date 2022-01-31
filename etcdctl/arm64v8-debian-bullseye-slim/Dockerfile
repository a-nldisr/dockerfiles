FROM arm64v8/debian:bullseye-slim
label maintainer "Rogier Dikkes <no-reply@0to1.nl>"

ENV ETCD_VERSION 3.5.1
ENV CPU_ARCH arm64

ADD https://github.com/coreos/etcd/releases/download/v${ETCD_VERSION}/etcd-v${ETCD_VERSION}-linux-${CPU_ARCH}.tar.gz /tmp/etcd.tar.gz

RUN apt-get update \
	&& rm -rf /var/lib/apt/lists/* \
    && tar zxvf /tmp/etcd.tar.gz -C /tmp && \
    mv /tmp/etcd-v${ETCD_VERSION}-linux-${CPU_ARCH}/etcdctl /usr/local/bin/etcdctl && \
    chmod a+x /usr/local/bin/etcdctl

ENTRYPOINT ["/usr/local/bin/etcdctl"]