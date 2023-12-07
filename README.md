# local-stack

## Getting Started

### Prerequisites
* Need docker setup locally

### Running localstack using docker
```shell
docker run --rm -it -p 4566:4566 -p 4571:4571 localstack/localstack
```

### Commands Required
* Create a s3 bucket
```
aws --endpoint-url=http://localhost:4566 s3api create-bucket --bucket my-bucket --region us-east-1
```
* List S3 buckets

```
aws --endpoint-url=http://localhost:4566 s3api list-buckets
```

* Create SQS

```
aws --endpoint-url=http://localhost:4566 sqs create-queue my-local-sqs-queue --region us-east-1
```

* List SQS

```
aws --endpoint-url=http://localhost:4566 sqs list-queues  
```