# **AWS Solution Architect**
Author: Phai Chaimongkol

Last Updated: 17-02-2022

## **Creating multiple AWS Accounts using one Gmail**

Every time you go to create an AWS Account you will be asked to use a unique email. You may be fine with using several email addresses but for some people they may prefer to receive any emails regarding their AWS accounts all on one email.

This is where the trick to using a + sign to create an infinite number of gmail accounts comes in. 

For example, if you have a Gmail account called example@gmail.com. You could create multiple unique email addresses from it by putting a + sign within that email address such as example+dev@gmail.com. This will allow you to consolidate all your emails for all your AWS accounts into one main email address. 

## **Securing your account with MFA**

Your AWS account as well as any roles that you may have set up within the account should be configured to use MFA. There are two main kinds of MFAs:
  
  - Software
  - Hardware

Software MFA is technically not proper MFA but it is better than using just your username and password. Software MFAs include things like Microsoft Authenticator, Fortitoken, Google Authenticator, etc.

Hardware MFAs includes devices such as Yubikey which generates a six-digit numeric code based upon a time-synchronised one-time password algorithm. For production account it is recommended that a hardware MFA device is used. 

## **Budgets**

Budgets on AWS is a way for you control your spending on AWS. It is a good practice to set a budget especially for specific services to ensure that you do not get hit with a huge bill. For example, you could set a budget on an AWS Relation Database Service (RDS) to something like $USD10/month. Additionally, you can also create a fixed account wide budget. 

You can set up a budget threshold alert to notify you when a specific budget threshold has been reached. Ideally you would want to set one at least one budget thresh hold at 50% and another at 80% as a second reminder. 

# **IAM**

Identity Access Management. This is a ```globally resilience  service``` (any data is always secured across all AWS regions) that is used to generate users, roles, and groups that are used on an AWS account. 

Originally when you first create your AWS you are signed in as a ```Root User```. However, a Root user has complete unrestricted access. As such, it is best to create multiple IAM roles or users with least privilidged configuration. 

Your AWS account has full trust on your IAM. As such, IAM as a service can have the same permissions as the root user with exception to billing and payment. 

- No Cost
- Global Service / Global resilience
- Allow or Deny its identities on AWS account
- No direct control on external accounts or users
- Identity federation and MFA

### **IAM User**

An IAM user is an identity which present humans or applications that need access to your account. An access and secret key can be generated for an IAM user which can then be used for AWS CLI or AWS SDK.

### **IAM Group**

Collection of related users e.g. development team, finance or HR. Each IAM Groups will often have its own set of permissions that have been configured to be least privileged to ensure that each group can only perform their intended tasks.

### **IAM Role**

Can be used by AWS Services, or for granting external access to your account. A role can be used to grant access to your account to an uncertain number of entities. For example, if you want all EC2 in your account to be able to access the S3 bucket, then you can create an IAM role with permission to S3 and use that role within all of your EC2s. 

### **IAM Policy**

IAM Policies essentially a document that used to alow or deny access to AWS services. These policies are attached to IAM User, Group and Role. On its own IAM Policy cannot do anything.

