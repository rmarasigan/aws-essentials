# Protect the AWS Root User
When you configure access to any account, two terms come up frequently – **authentication** and **authorization**. While these terms might seem basic, you must fully understand them to properly configure access management on AWS.

## Authentication
**Authentication** ensures that the user is who they say they are. User names and passwords are the most common types of authentication, but you might also work with other forms, such as token-based authentication or biometric data, like a fingerprint. Authentication simply answers the question, *“Are you who you say you are?”*

## Authorization
**Authorization** is the process of giving users permission to access AWS resources and services. Authorization determines whether a user can perform certain actions, such as read, edit, delete, or create resources. Authorization answers the question, “What actions can you perform?”

## AWS root user
When you first create an AWS account, you begin with a single sign-in identity that has complete access to all AWS services and resources in the account. This identity is called the AWS root user and is accessed by signing in with the email address and password that you used to create the account.

### AWS root user credentials
The AWS root user has two sets of credentials associated with it. One set of credentials is the ***email address and password*** used to create the account. This allows you to access the AWS Management Console. The second set of credentials is called ***access keys***, which allow you to make programmatic requests from the AWS Command Line Interface (AWS CLI) or AWS API.

Access keys consist of two parts:
* Access key ID
* Secret access key

Similar to a user name and password combination, you need both the access key ID and secret access key to authenticate your requests via the AWS CLI or AWS API. Access keys should be managed with the same security as an email address and password.

### Best practices when working with the AWS root user
The root user has complete access to all AWS services and resources in your account, in addition to your billing and personal information. Due to this, you should securely lock away the credentials associated with the root user and do not use the root user for everyday tasks.

To ensure the safety of the root user, follow these best practices:
* Choose a strong password for the root user
* Never share your root user password or access keys with anyone
* Disable or delete the access keys associated with the root user
* Do not use the root user for administrative tasks or everyday tasks

### Delete your keys to stay safe
If you don't have an access key for your AWS account root user, don't create one unless you absolutely need to. If you have an access key for your AWS account root user and want to delete the keys, follow these steps:

1. In the AWS Management Console, go to the **My Security Credentials** page, and sign in with the root user’s email address and password.
2. Open the **Access keys** section.
3. Under **Actions**, choose **Delete**.
4. Choose **Yes**.

## Multi-factor authentication (MFA)
When you create an AWS account and first log in to the account, you use single-factor authentication. Single-factor authentication is the simplest and most common form of authentication. It only requires one authentication method. In this case, you use a user name and password to authenticate as the AWS root user. Other forms of single-factor authentication include a security pin or a security token. Using multi-factor authentication (MFA) is important in preventing unwanted account access.

MFA requires two or more authentication methods to verify an identity. MFA pulls from the following three categories of information:
* Something you know, such as a user name and password, or pin number
* Something you have, such as a one-time passcode from a hardware device or mobile app
* Something you are, such as fingerprint or face scanning technology

This extra layer of security can help protect your most important accounts, which is why you should enable MFA on your AWS root user.

### MFA on AWS
Enabling MFA adds an additional layer of security because it requires users to use a supported MFA mechanism in addition to their regular sign-in credentials. Enabling MFA on the AWS root user account is an AWS best practice.

### Supported MFA devices
AWS supports a variety of MFA mechanisms, such as virtual MFA devices, hardware devices, and Universal 2nd Factor (U2F) security keys.

#### Virtual MFA
A software app that runs on a phone or other device that provides a one-time passcode. These applications can run on unsecured mobile devices, and because of that, they might not provide the same level of security as hardware or U2F devices.

**Supported Devices**: Authy, Duo Mobile, LastPass Authenticator, Microsoft Authenticator, Google Authenticator

#### Hardware
A hardware device, generally a key fob or display card device, that generates a one-time, six-digit numeric code.

**Supported Devices**: Key fob, display card 

#### U2F
A hardware device that you plug in to a USB port on your computer.

**Supported Devices**: YubiKey

## Resources
* [Enabling a Hardware MFA Device (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_physical.html)
* [Enabling a U2F Security Key (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_u2f.html)
* [Enabling a Virtual Multi-Factor Authentication (MFA) Device (Console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html)
* [Table of Supported MFA Devices](https://aws.amazon.com/iam/features/mfa/)