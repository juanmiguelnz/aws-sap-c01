
### Static Website
1. Create a new S3 bucket.
2. Enable Static web hosting and set an index.html file.
3. Set the Block public access setting to "Off".
4. Set Bucket policy permissions to allow public acccess
```
{
    "Version": "2012-10-17",
    "Id": "S3PolicyId1",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": [
                "arn:aws:s3:::<S3BucketName>",
                "arn:aws:s3:::<S3BucketName>/*"
            ]
        }
    ]
}
```
! Test

5. 
