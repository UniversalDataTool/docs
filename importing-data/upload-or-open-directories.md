---
description: Open directories or upload files to your Universal Data Tool dataset
---

# Upload or Open Directories

## Uploading Files

The best way to upload files is via the "Upload to S3" dialog, which requires that you connect your S3 bucket to the Universal Data Tool. You can find details on how to do that in the [Import from S3 guide](import-from-aws-s3-bucket.md).

![Import files Dialog](../.gitbook/assets/image%20%2840%29.png)

## Opening Files

You can only open files in the desktop application, because web apps aren't allowed to access filesystem directories. To select a directory full of files, use the `Samples > Import from Directory` button.

{% hint style="warning" %}
If you Import files from Directory your UDT dataset will use "links" to files on your system, this means they won't be very accessible if you're sharing your dataset or using it on multiple computers.
{% endhint %}

