# CDK Reference

## AWS cdk install

```bash
npm install -g aws-cdk
```

## API Reference

https://docs.aws.amazon.com/cdk/api/latest/python/index.html

## Create App - [AWS Reference](https://docs.aws.amazon.com/cdk/latest/guide/hello_world.html)

```bash
mkdir hello-cdk
cd hello-cdk
cdk init app --language python
source .venv/bin/activate
python -m pip install -r requirements.txt
```

## Add an Amazon S3 bucket

```bash
pip install aws-cdk.aws-s3
```

Replace the first import statement in hello_cdk_stack.py in the hello_cdk directory with the following code.

```python
from aws_cdk import (
    aws_s3 as s3,
    core as cdk
)

bucket = s3.Bucket(self,
    "MyFirstBucket",
    versioned=True,)

```

## Synthesize and Deploy

```bash
cdk synth
cdk deploy
```
