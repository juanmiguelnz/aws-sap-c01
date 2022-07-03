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



#### See:
* [Use Azure AD as AWS Identity Provider](https://www.youtube.com/watch?v=ebmvM22KFHk)
* [SAML Federation Azure AD](https://aws.amazon.com/blogs/security/how-to-automate-saml-federation-to-multiple-aws-accounts-from-microsoft-azure-active-directory/)
* [Microsoft Docs](https://docs.microsoft.com/en-us/azure/active-directory/saas-apps/amazon-web-service-tutorial)
