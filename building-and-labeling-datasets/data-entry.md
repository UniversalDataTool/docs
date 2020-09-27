---
description: Do any type of data entry with the Universal Data Tool
---

# Data Entry

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Data Entry button from the `Setup > Data Type` page.

![](../.gitbook/assets/image%20%2822%29.png)

You can configure the Data Entry to create the right interface for your dataset. Use the `Setup > Preview` button to see your interface against either an example image or a sample from your dataset.

![Configure the Data Entry interface](../.gitbook/assets/image%20%2869%29.png)

You can add a variety of different inputs by clicking the "Add Input" button.

![Input types available when you click Add Input](../.gitbook/assets/image%20%2861%29.png)

## Import Data

You can use virtually any method of importing for data entry datasets, here is a list of common import methods.

* [Import from AWS S3 Bucket](../importing-data/import-from-aws-s3-bucket.md)
* [Import from List of URLs](../importing-data/import-file-urls.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)
* [Upload or Open Directory](../importing-data/upload-or-open-directories.md)
* [Import from Google Drive](../importing-data/import-from-google-drive.md)

## Label your Data \(with friends!\)

![Example Data Entry Sample](../.gitbook/assets/image%20%2862%29.png)

## Export and Use

You can use either JSON or CSV to export the Data Entry type. See the full [Data Entry JSON Specification](https://github.com/UniversalDataTool/udt-format/blob/master/interfaces/data_entry.md) for how the Data Entry JSON is formatted.

Each JSON sample looks like the following:

```javascript
{
    "pdfUrl": "https://...", // or imageUrl, document etc.
    
    "annotation": { "FieldName": "..." }
}
```

