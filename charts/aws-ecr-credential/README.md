# aws-ecr-credential

This Chart seemlessly integrate Kubernetes with AWS ECR

Simply deploy this chart to your kubernetes cluster and you will be able to pull and run images from your AWS ECR (Elastic Container Registry) in your cluster.

## Usage

Run the following commands to install this chart

```sh
helm repo add aws-ecr https://djschaap.github.io/aws-ecr-credential
helm repo update

helm install --name aws-ecr-credential aws-ecr/aws-ecr-credential \
  --set-string aws.account=<aws account nubmer> \
  --set aws.region=<aws region> \
  --set aws.accessKeyId=<base64> \
  --set aws.secretAccessKey=<base64> \
  --set targetNamespace=default
```

That chart will create a Secret in targetNamespace named `aws-registry`.

In your kubernetes Deployment Pod spec, use `imagePullSecrets: aws-registry`.

Example:
```yaml
apiVersion: apps/v1
kind: Deployment
spec:
  template:
    spec:
      imagePullSecrets:
      - name: aws-registry
      containers:
        - name: node
          image: node:latest
```
