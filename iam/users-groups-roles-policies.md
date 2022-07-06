### IAM Roles and Cross-account Access

#### Trusted Account vs Trusting Account
* Trusted Account - This is where the users are created. A Policy with the ARN of the IAM Role (from the Trusting Account) is created and assigned to the user or group.
* Trusting Account - This is where IAM roles are created that can be "assumed" by the users from the Trusted Accoount to be able to create resources.

#### Steps
1. From the Trusting Account create an IAM Role with the permissions that you want the users from the Trusted Account to be able to assume.
2. From the Trusted Account, create a new Policy with the ARN of the IAM Role from the Trusting Account.
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "sts:AssumeRole",
            "Resource": "arn:aws:iam::<TrustingAccountID>:role/<IAMRoleName>"
        }
    ]
}
```
3. From the Trusted Account, assign the Policy to a user or a group. 
4. Log in using a user with the permission to "assume" the Role and try to switch roles.




#### See:
* [Securing and Managing Your AWS Account](https://app.pluralsight.com/paths/certificate/aws-certified-solutions-architect-professional#:~:text=2.%20Securing-,and,-Managing%20Your%20AWS)
* [Youtube Playlist](https://www.youtube.com/playlist?list=PLzde74P_a04cKnuXyi--fkIoY1sxztyqL)
