FROM amazon/aws-cli:2.1.25
LABEL maintainer="djschaap@users.noreply.github.com"

# Install kubectl
RUN curl -LO https://dl.k8s.io/release/v1.20.2/bin/linux/amd64/kubectl \
	&& mv kubectl /usr/local/bin \
	&& chmod 0555 /usr/local/bin/kubectl
