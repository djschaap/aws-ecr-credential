FROM amazon/aws-cli:2.0.23
LABEL maintainer="djschaap@users.noreply.github.com"

# Install kubectl
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.18.4/bin/linux/amd64/kubectl \
	&& mv kubectl /usr/local/bin \
	&& chmod +x /usr/local/bin/kubectl
