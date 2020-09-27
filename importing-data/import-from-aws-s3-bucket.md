---
description: Import samples from an S3 bucket directly into the Universal Data Tool!
---

# Import from AWS S3 Bucket

## Overview

If you have an S3 Bucket full of data to label, we'll need to do a couple of things to make that data accessible to UDT.

1. Configure the bucket so the files can be loaded
2. Create a user \(or use an existing user\) that can access the bucket
3. Import the data into S3

It should only take a couple minutes, let's do it!

## 1. Configure Bucket

First we need to make sure our files can be loaded from the web. To do this, we need to add a CORs policy in our Bucket Permissions. We can do this from the web on the [AWS Buckets page](https://s3.console.aws.amazon.com/s3/buckets/).

You can paste these CORs permissions in to make files web-accessible.

```text
<?xml version="1.0" encoding="UTF-8"?>
<CORSConfiguration xmlns="http://s3.amazonaws.com/doc/2006-03-01/">
<CORSRule>
    <AllowedOrigin>*</AllowedOrigin>
    <AllowedMethod>GET</AllowedMethod>
    <AllowedMethod>HEAD</AllowedMethod>
    <AllowedMethod>PUT</AllowedMethod>
    <AllowedMethod>POST</AllowedMethod>
    <AllowedMethod>DELETE</AllowedMethod>
    <AllowedHeader>*</AllowedHeader>
</CORSRule>
</CORSConfiguration>
```

![Paste the CORs configuration in here](../.gitbook/assets/image%20%2837%29.png)

After you save that, you can pick the directories you'd like to be accessible by clicking on the directory, then clicking `Actions > Make Public` If your entire bucket is public, you can skip this step.

![This will create URLs for each item in your S3 bucket.](../.gitbook/assets/image%20%2830%29.png)

## 2. Add IAM Credentials

Next, we need to get the keys to allow the UDT to browse for the S3 bucket files. We can do this by copying our AWS Access Key and Secret Access Key.

{% hint style="warning" %}
It's a good idea to limit the permissions of the user you're getting the access keys from, that way this key can only be used for it's intended purpose!
{% endhint %}

Navigate to the IAM service and select \(or create\) a user. The user must have permissions to access S3 buckets. Then click Create Access Key to create your keys!

{% hint style="danger" %}
One simple, but dangerous way to give the AWS permissions is to give the S3FullAccess permission, as show below. Fine-grained permissions are more secure!

![](../.gitbook/assets/image%20%2845%29.png)
{% endhint %}

![Clicking Create Access Key will create the keys you need](../.gitbook/assets/image%20%2834%29.png)

## 3. Add Keys to the Universal Data Tool

Navigate to [udt.dev](https://udt.dev) or open the UDT. Click "Add Authentication" and paste your keys. 

![Add Authentication Dialog](../.gitbook/assets/image%20%2838%29.png)



## 4. Browse Buckets and Import

You can now create a new UDT Dataset and navigate to `Samples > Import from S3` \(which will be enabled\). You'll be able to select from all the buckets accessible to this user.

![You can select any buckets accessible to that user.](../.gitbook/assets/image%20%2843%29.png)

![You can then import files from S3 directories.](../.gitbook/assets/image%20%2828%29.png)

## Bonus: Import via Uploading to S3

You can also upload to S3 directly from the UDT, after doing so, your files will automatically be added to your UDT dataset.

![Use the Upload to S3 to directly add files to UDT!](../.gitbook/assets/image%20%2847%29.png)







