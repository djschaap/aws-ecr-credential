# aws-kubectl image

## Build image
```bash
DOCKER_HUB_USER=CHANGEME
VERSION=2.0.23-1.18.4
docker build -t ${DOCKER_HUB_USER}/aws-kubectl:${VERSION} aws-kubectl && \
  docker push ${DOCKER_HUB_USER}/aws-kubectl:${VERSION}
```
