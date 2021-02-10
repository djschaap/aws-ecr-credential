# aws-kubectl Image

Docker Hub will build an image automatically whenever a new tag
matching `/^aws-kubectl-[0-9.]+-[0-9.]+$/` is pushed to GitHub.

It will be published to https://hub.docker.com/repository/docker/djschaap/aws-kubectl .

## Build Image Manually
```bash
docker build -t aws-kubectl aws-kubectl
```
