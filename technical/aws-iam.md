# Identity and Access Management
**AWS Identity and Access Management (IAM)** is an AWS service that helps you manage access to your AWS account and resources. It also provides a centralized view of who and what are allowed inside your AWS account (authentication), and who and what have permissions to use and work with your AWS resources (authorization).

With IAM, you can share access to an AWS account and resources without sharing your set of access keys or password. You can also provide granular access to those working in your account, so people and services only have permissions to the resources they need.

## Features
* IAM is global and not specific to any one Region. You can see and use your IAM configurations from any Region in the AWS Management Console.
* IAM is integrated with many AWS services by default.
* You can establish password policies in IAM to specify complexity requirements and mandatory rotation periods for users.
* IAM supports MFA.
* IAM supports identity federation, which allows users who already have passwords elsewhere – for example, in your corporate network or with an internet identity provider – to get temporary access to your AWS account.
* Any AWS customer can use IAM; the service is offered at no additional charge.

## User
An **IAM user** represents a person or service that interacts with AWS. You define the user in your AWS account. Any activity done by that user is billed to your account. Once you create a user, that user can sign in to gain access to the AWS resources inside your account.

## User Credentials
An **IAM user** consists of a name and a set of credentials. When you create a user, you can provide them with the following types of access:
* Access to the AWS Management Console
* Programmatic access to the AWS Command Line Interface (AWS CLI) and AWS application programming interface (AWS API)

To access the AWS Management Console, provide the user with a user name and password. For programmatic access, AWS generates a set of access keys that can be used with the AWS CLI and AWS API. IAM user credentials are considered permanent, which means that they stay with the user until there’s a forced rotation by admins.

## Groups
An **IAM group** is a collection of users. All users in the group inherit the permissions assigned to the group. This makes it possible to give permissions to multiple users at once. It’s a more convenient and scalable way of managing permissions for users in your AWS account. This is why using IAM groups is a best practice.

Keep in mind the following features of groups:
* Groups can have many users.
* Users can belong to many groups.
* Groups cannot belong to groups.

The root user can perform all actions on all resources inside an AWS account by default. This is in contrast to creating new IAM users, new groups, or new roles. New IAM identities can perform no actions inside your AWS account by default until you explicitly grant them permission.

## Policies
To manage access and provide permissions to AWS services and resources, you create IAM policies and attach them to IAM users, groups, and roles. Whenever a user or role makes a request, AWS evaluates the policies associated with them.

**Example**
```json
{
   "Version": "2012-10-17",
   "Statement": [{
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
   }]
}
```

This policy has four major JSON elements: **Version**, **Effect**, **Action**, and **Resource**.

* The **Version** element defines the version of the policy language. It specifies the language syntax rules that are needed by AWS to process a policy. To use all the available policy features, include **"Version": "2012-10-17"** before the **"Statement"** element in your policies.
* The **Effect** element specifies whether the statement will allow or deny access. In this policy, the Effect is **"Allow"**, which means you’re providing access to a particular resource.
* The **Action** element describes the type of action that should be allowed or denied. In the example policy, the action is **"*"**. This is called a *wildcard*, and it is used to symbolize every action inside your AWS account.
* The **Resource** element specifies the object or objects that the policy statement covers. In the policy example, the resource is the wildcard **"*"**. This represents all resources inside your AWS console.

### Policy Structure
| Element  	      | Description                                                              	| Required  |
|--------------	|--------------------------------------------------------------------------	|----------	|
| **Effect**   	| Specifies whether the statement results in an allow or an explicit deny  	|    √      |
| **Action**   	| Describes the specific actions that will be allowed or denied            	|    √      |
| **Resource**  	| Specifies the object or objects that the statement covers                	|    √      |

## Resources 
* [What Is IAM?](https://docs.aws.amazon.com/en_us/IAM/latest/UserGuide/introduction.html)
* [AWS IAM Identities](https://docs.aws.amazon.com/en_us/IAM/latest/UserGuide/id.html)
* [Access Management with AWS IAM](https://docs.aws.amazon.com/en_us/IAM/latest/UserGuide/access.html)