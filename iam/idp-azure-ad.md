## Azure AD as Identity Provicer

### Steps:
#### 1. Create Azure AD Enterprise Application
  * From Azure AD, create an Enterprise Application and use the "AWS Single-Account Access" template.
  * Once created, from the Overview section of the Enterprise Application select "Set up single sign on".
  * Select SAML.
  * In the "Basic SAML Configuration", edit the "Identifier (Entity ID)" field. The URL must be unique in your environment. (Example: https://signin.aws.amazon.com/awssaml1).
  * Download the Federation Metadata XML file.

#### 2. Add Identity Provider
  * From the AWS IAM Dashboard, go to Identity Providers. Click Add Provider.
  * Give the Provider a name and upload the Federation Metadata XML file. Click Add Provider.

#### 3. Create an AWS IAM Role
These are the IAM Roles that syncs back to Azure AD and be assigned to Azure users.

#### 4. Create an AWS IAM User
This user will be used by Azure AD to connect to AWS to list the IAM Roles. Follow least privilege guidelines.
  * Create the a new IAM User with list role permissions
  * Create Access Key
  * Take note Access Key ID and Secret

#### 5. Provision
  * From Azure AD, click Provisioning. Select "Automatic" as Provisioning Mode.
  * Use the Access Key ID and Secret sa credentials.
  * Click Start Provisioning


#### See:
* [Use Azure AD as AWS Identity Provider](https://www.youtube.com/watch?v=ebmvM22KFHk)
* [SAML Federation Azure AD](https://aws.amazon.com/blogs/security/how-to-automate-saml-federation-to-multiple-aws-accounts-from-microsoft-azure-active-directory/)
* [Microsoft Docs](https://docs.microsoft.com/en-us/azure/active-directory/saas-apps/amazon-web-service-tutorial)
