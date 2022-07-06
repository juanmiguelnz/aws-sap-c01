### IAM Roles and Cross-account Access

#### Trusted Account vs Trusting Account
* Trusted Account - This is where the users are created. A Policy with the ARN of the IAM Role (from the Trusting Account) is created and assigned to the user or group.
* Trusting Account - This is where IAM roles are created that can be "assumed" by the users from the Trusted Accoount to be able to create resources.

#### Steps
1. Create an IAM Role in the Trusting Account with the permissions that you want the users from the Trusted Account to be able to assume.
2. From the Trusted Account, create a new Policy with the ARN of the IAM Role from the Trusting Account
```

```
3. sdfsdf
4. 




#### See:
* [Securing and Managing Your AWS Account](https://app.pluralsight.com/paths/certificate/aws-certified-solutions-architect-professional#:~:text=2.%20Securing-,and,-Managing%20Your%20AWS)
* [Youtube Playlist](https://www.youtube.com/playlist?list=PLzde74P_a04cKnuXyi--fkIoY1sxztyqL)
