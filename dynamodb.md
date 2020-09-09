# DynamoDB

## intro

- noSQL key-value document database
- documents are structured JSON
- documents are stored in tables

## features

- very fast
- application level interfaces for db operations eg querying data, writing to tables/documents etc
- accessing data inside Dynamo requires AWS SDK with IAM authorisation

## pricing

- can pay for a reserved capacity or on demand
- reserved capacity is the max you think you'll need ie fixed costs
- on demand is based on actual usage ie no upper limit, but also no throttling

## alternatives

- see [S3](./s3.md) and [this good comparison with s3](https://serverless.pub/s3-or-dynamodb/)
- also [DocumentDB](https://aws.amazon.com/documentdb/) which is essentially AWS managed MongoDB. Comparison [here](https://searchaws.techtarget.com/tip/DocumentDB-vs-DynamoDB-Compare-AWS-NoSQL-databases)
