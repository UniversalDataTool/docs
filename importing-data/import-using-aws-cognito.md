---
description: Import and save samples to S3 buckets using AWS Cognito
---

# Import using AWS Cognito

### 1. Create a User Pool

Navigate to `Cognito` in AWS and click create Manage User Pools. Use whatever password settings are best for your organization.

![user pool](https://user-images.githubusercontent.com/1910070/82127422-5e7c4800-9781-11ea-96d3-ee12e97fbbda.png)

### 1.1 Create App Client

After creating the user pool, go to "App Clients" in the sidebar. Create an App Client, but make sure to do the following:

* Uncheck "Generate Client Secret"
* Check "Enable user password based authentication

![app client](https://user-images.githubusercontent.com/1910070/82192862-8f17cb00-98c2-11ea-8831-36166dfe78e7.png)

### 2. Create an Identity Pool

Navigate to Federated Idenitities in AWS and create an identity pool.

Create a new IAM role. Then review this role in IAM.

### 3. Create S3 Bucket

Create a bucket with public read permissions. In the "Permissions" tab, allow everyone to read and write objects to the S3 bucket.

Copy the [CORs configuration from the Amplify docs](https://docs.amplify.aws/lib/storage/getting-started/q/platform/js#using-amazon-s3)

### 4. Configure IAM Roles

Navigate to IAM panel by searching for the IAM service. You'll have a bunch of newly created Cognito roles. Use the instructions on the Amplify docs [getting started page and create an Auth and Unauth policy](https://docs.amplify.aws/lib/storage/getting-started/q/platform/js#using-amazon-s3) for your new IAM users.

Add each policy you copied with "Attach Policy" to the User Role. Make sure to replace the "example bucket name" with the name of your bucket.

Create the policy, give it a name like "UDTTestBucketRole".

### 5. Create Example User

In Cognito page click "Create User", enter the username and password. Mark the account as verified. You'll then be prompted with Complete your Sign Up.

