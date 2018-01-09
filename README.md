# Ubuntu Docker-CE Systemd

This image builds ontop of [thomasjpfan/ubuntu-python-systemd](https://github.com/thomasjpfan/ubuntu-python-systemd) to make it easier to test ansible playbooks that needs docker already installed.

## Latest Version

`thomasjpfan/ubuntu-docker-ce-systemd:16.04-docker-ce-17.12.0`

## Usage

```bash
docker run -d --rm --name ansible-docker --privileged \
    -v /sys/fs/cgroup:/sys/fs/cgroup:ro -t \
    thomasjpfan/ubuntu-docker-ce-systemd:16.04-docker-ce-17.12.0
```