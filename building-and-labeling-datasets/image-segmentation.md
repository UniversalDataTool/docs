---
description: Segment instances on image datasets using the Universal Data Tool
---

# Image Segmentation

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Image Segmentation button from the `Setup > Data Type` page.

![](../.gitbook/assets/image%20%2822%29.png)

You can configure the Image Segmentation to create the right interface for your dataset. Use the `Setup > Preview` button to see your interface against either an example image or a sample from your dataset.

![Image Segmentation with Bounding Box Classification](../.gitbook/assets/image%20%2823%29.png)

#### Configuring Regions and Labels

The Image Segmentation interface allows different types of regions, the options for regions are:

* bounding-box
* polygon
* point

Each region can any number of labels, which can be configured under "Available Labels"

![](../.gitbook/assets/image%20%2826%29.png)

## Import Data

You can use any of the following methods to import image data. If you're just getting started, you can quickly create a dataset using the COCO Images method!

* [Import COCO Dialog](../importing-data/coco-images.md)
* [Import from Google Drive](../importing-data/import-from-google-drive.md)
* [Import from AWS S3 Bucket](../importing-data/import-from-aws-s3-bucket.md)
* [Import from List of URLs](../importing-data/import-file-urls.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)
* [Upload or Open Directory](../importing-data/upload-or-open-directories.md)

## Label your Data!

Use the `Label` tab to label your data.



## Export and Use

You can download your data using the download icon at the top.

![Download your data in CSV or JSON format to use the annotations](../.gitbook/assets/image%20%2844%29.png)

You can use the [Universal Data Tool Converter](https://universaldatatool.com/convert) to convert UDT files into PNG masks, or other formats that are helpful for machine learning datasets.

![It&apos;s very common to convert into PNGs](../.gitbook/assets/image%20%2829%29.png)

