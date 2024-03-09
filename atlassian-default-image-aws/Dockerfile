FROM atlassian/default-image:4

ARG DEBIAN_FRONTEND="noninteractive"
ARG CFLAGS="-march=native -mtune=generic"

RUN mkdir --parent /tmp/awscli && \
    curl --silent --fail --show-error --location \
        --output /tmp/awscli/awscliv2.zip \
        --url "https://awscli.amazonaws.com/awscli-exe-linux-$(uname --machine).zip" && \
    unzip -d /tmp/awscli/ /tmp/awscli/awscliv2.zip && \
    /tmp/awscli/aws/install && \
    rm --recursive --force /tmp/awscli
