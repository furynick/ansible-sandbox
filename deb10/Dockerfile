# docker run -d --name systemd-debian --tmpfs /tmp --tmpfs /run --tmpfs /run/lock -v /sys/fs/cgroup:/sys/fs/cgroup:ro jrei/systemd-debian:10
FROM jrei/systemd-debian:10

RUN apt-get update && apt-get install -y openssh-server && \
    apt-get clean && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/lib/apt/lists/*

RUN install -o root -g root -m 0700 -d /root/.ssh

COPY --chown=root:root authorized_keys /root/.ssh
