# boto3

## intro

python library developed by AWS for interacting with AWS services from code

## features

- exposes two different interfaces: `client` and `resource`

### client

- the lowest level interface
- methods generally map 1:1 with AWS service APIs

example:

```python
import boto3

client = boto3.client('s3')
response = client.list_objects_v2(Bucket='mybucket')
for content in response['Contents']:
    obj_dict = client.get_object(Bucket='mybucket', Key=content['Key'])
    print(content['Key'], obj_dict['LastModified'])
```

*Note: in the above example,* `list_objects_v2` *method only returns max 1000 objects and would require additional code to get all objects in the bucket. This is an example of the limitations of the* `client` *interface.*

### resource

- higher level, more pythonic and object oriented interface
- generally recommended for use, but not always available for all services

```python
import boto3

s3 = boto3.resource('s3')
bucket = s3.Bucket('mybucket')
for obj in bucket.objects.all():
    print(obj.key, obj.last_modified)

```
