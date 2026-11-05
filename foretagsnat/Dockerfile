FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    iproute2 \
    iputils-ping \
    openssh-client \
    openssh-server \
    curl \
    nginx \
    sudo \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash student \
    && echo "student:student" | chpasswd

RUN mkdir -p /run/sshd

CMD ["sleep", "infinity"]
