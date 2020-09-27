---
description: Segment objects or parts of a video with the Universal Data Tool
---

# Video Segmentation

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Video Segmentation button from the `Setup > Data Type` page.

![](../.gitbook/assets/image%20%2822%29.png)

You can configure the Video Segmentation to create the right labels or segmentation region types for your dataset. Use the `Setup > Preview` button to see your interface against either an example image or a sample from your dataset.

#### Configuring Regions and Labels

The Video Segmentation interface allows different types of regions, the options for regions are:

* bounding-box
* polygon
* point

Each region can any number of labels, which can be configured under "Available Labels"

![Configure Video Segmentation Interface](../.gitbook/assets/image%20%2857%29.png)

## Import Data

You can use any of the following methods to import video data.

* [Import File URLs](../importing-data/import-file-urls.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)

## Label your Data \(with friends!\)

The easiest way to use a Video Segmentation dataset is using the JSON or CSV format. You can use the timeline at the top to go to different frames of the video. Regions will automatically interpolate between frames.

![](../.gitbook/assets/image%20%2866%29.png)



## Export and Use

Use the "Download JSON" or "Download CSV" button at the top when you're done labeling.



