FROM hashicorp/terraform:latest

RUN mkdir --parent /tmp/awscli && \
    wget --output-document /tmp/awscli/awscliv2.zip \
        "https://awscli.amazonaws.com/awscli-exe-linux-$(uname --machine).zip" && \
    unzip -d /tmp/awscli/ /tmp/awscli/awscliv2.zip && \
    /tmp/awscli/aws/install --update && \
    rm -rf /tmp/awscli

ENTRYPOINT ["/bin/sh"]
