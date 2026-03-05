FROM docker.io/ubuntu:focal@sha256:8feb4d8ca5354def3d8fce243717141ce31e2c428701f6682bd2fafe15388214

RUN \
  apt-get update && \
  apt-get install -y \
    ca-certificates \
    iproute2 \
    python3 \
    python3-cryptography

ADD https://raw.githubusercontent.com/gdraheim/docker-systemctl-replacement/master/files/docker/systemctl3.py /usr/bin/systemctl
RUN chmod +x /usr/bin/systemctl
CMD ["/usr/bin/systemctl", "--init"]
