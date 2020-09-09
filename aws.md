# AWS lambda

## intro

Can develop directly in AWS console. Small simple functions to handle "events".
Events are JSON requests

```python
import json

def lambda_handler(event, context):
    # TODO implement
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }

```

## invoking



# Sagemaker

- triggering
- multi threading
- storage
-
