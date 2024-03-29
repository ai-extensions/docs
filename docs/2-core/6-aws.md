# Access to Object Storage

## Introduction
A dedicated object storage (in this example Amazon S3) is pre-configured to be accessed from the App Hub. This can be done with the Amazon Web Server (AWS) `aws s3` commands in the AWS CLI.

## Practical Example
For example, to list the content of a specific S3 bucket, you can use the command below.
```
aws s3 ls <bucket_name>
```
Other examples with full syntax on using the `aws s3` command are described in the official [AWS website](https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html).