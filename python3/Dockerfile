FROM thomasjpfan/ubuntu-python-systemd:16.04-py3

ENV DOCKER_CHANNEL stable
ENV DOCKER_VERSION 17.12.0~ce-0~ubuntu

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    software-properties-common apt-transport-https curl && \
    rm -Rf /var/lib/apt/lists/* && \
    rm -Rf /usr/share/doc && rm -Rf /usr/share/man && \
    apt-get clean

RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) \
    ${DOCKER_CHANNEL}" && \
    apt-get update && \
    apt-get install -y --no-install-recommends \
    docker-ce=${DOCKER_VERSION} && \
    rm -Rf /var/lib/apt/lists/* && \
    rm -Rf /usr/share/doc && rm -Rf /usr/share/man && \
    apt-get clean
