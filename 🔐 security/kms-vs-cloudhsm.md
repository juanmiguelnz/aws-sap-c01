### KMS vs CloudHSM
| KMS      | CloudHSM |
| ----------- | ----------- |
| Multi-tenant | Single-tenant |
| Master key cannot be exported | Master key can be exported|
| FIPS 140-2 Level 2 | FIPS 140-2 Level 2|
| Regional endpoint | Faster - hooked up to you VPC|
| Only the KMS service has access to the HSM | Direct HSM access with APIs|

### Exercise
1. Create an S3 bucket
2. Create an IAM role (if you haven't already) that has read/write permissions to the S3 bucket
3. Create a customer managed key in KMS and give key usage permission to the IAM role you just created
4. Create a new EC2 instance and set the IAM instance profile to the IAM role you just created
5. Log in to the EC2 instance and try to upload a file with server-side encryption enabled
```
aws s3 cp <your_sample_file.txt> s3://<your_s3_bucket> --sse aws:kms --sse-kms-key-id "<kms_key_id>"
```
6. From the AWS console, go to S3 and check the properties of the file you just uploaded and you can see SSE is enabled

### See
* [YouTube - Encrypt & Decrypt Data with KMS](https://www.youtube.com/watch?v=0VKJfpCoF2s)
