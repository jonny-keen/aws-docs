# AWS lambda

## intro

- Can develop directly in AWS console or deploy a compiled package.
- Small simple functions to handle "events".
- Events are JSON requests of any predefined format.

AWS hello world example below.

```python
import json

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }

```

`context` is an object supplied by AWS which "*provides methods and properties that provide information about the invocation, function, and execution environment.*"

## invoking

- can be invoked synchonously ie. make request and wait for response
- or asynchronously ie. make request and lambda handles the output

- for async calls, lambda has an internal queueing system with a configurable numbers of retries and retention periods.

## other feature

- supports environment variables
- supports multi-threading
- stateless
- can publish multiple versions to allow versioning

## pricing

You only pay for the computation used when running the function ie. pay nothing until the lambda is run.

## limitations

lambda has [certain limitations](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html)
