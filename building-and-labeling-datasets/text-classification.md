---
description: Classify text using the Universal Data Tool
---

# Text Classification

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Text Classification button from the `Setup > Data Type` page.

![](../.gitbook/assets/image%20%2822%29.png)

You can now configure the interface you'd like for you Text Classification dataset by adding any classifications you'd like to display per sample, as well as configure if multiple classifications are allowed to be selected.

![Text Classification Configuration](../.gitbook/assets/image%20%2865%29.png)



## Import Data

You can use any of the following methods to import text data. If you're just getting started, you can quickly create a dataset using the COCO Images method!

* [Import Text Snippets](../importing-data/import-text-snippets.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)

## Label your Data \(with friends!\)

Go to the `Label` tab to begin labeling data. See the [Collaborative Labeling Guide](../collaborative-labeling.md) to label with friends or a team of your labelers.

![An example Text Classification interface](../.gitbook/assets/image%20%2855%29.png)



## Export and Use

Text Classification can easily be exported and read as a CSV or JSON file.

For example, if you export as a CSV you'll get a table that looks like the following:

| path | document | annotation |
| :--- | :--- | :--- |
| samples.0 | This has made me so happy. I love it. | positive\_sentiment |
| samples.1 | I hate this thing. It's so bad. | negative\_sentiment |

