ARG BASE=ubuntu:24.04
FROM $BASE
RUN apt-get -y update \
    && apt-get -y install openvswitch-common libpcap0.8 libxml2 libvirt0 libc6 \
    && rm -rf /var/lib/apt/lists/*
COPY skydive /usr/bin/skydive
COPY skydive.yml /etc/skydive.yml
ENTRYPOINT ["/usr/bin/skydive", "--conf", "/etc/skydive.yml"]
