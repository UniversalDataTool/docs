---
description: Label words or phrases within text using the Universal Data Tool
---

# Named Entity Recognition

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Named Entity Recognition button from the `Setup > Data Type` page.

![Select Named Entity Recognition when choosing an interface](../.gitbook/assets/image%20%2822%29.png)

You can now configure the interface you'd like for you Named Entity Recognition dataset by adding any labels you'd like to display per sample.

![Named Entity Recognition Configuration](../.gitbook/assets/image%20%2859%29.png)

## Import Data

You can use any of the following methods to import text data.

* [Import Text Snippets](../importing-data/import-text-snippets.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)

## Label your Data \(with friends!\)

Go to the `Label` tab to begin labeling data. See the [Collaborative Labeling Guide](../collaborative-labeling.md) to label with friends or a team of your labelers.

![Named Entity Recognition Example Interface](../.gitbook/assets/image%20%2858%29.png)

## Export and Use

The easiest way to use a Named Entity Recognition dataset is using the JSON format. Use the "Download JSON" button at the top when you're done labeling and check out the [Named Entity Recognition JSON Specification](https://github.com/UniversalDataTool/udt-format/blob/master/interfaces/text_entity_recognition.md).

Here's what a JSON sample looks like in the resultant dataset:

```javascript
{
  "document": "This strainer makes a great hat, I'll wear it while I serve spaghetti",
  "annotation": {
    "entities": [
      { text: "strainer", label: "hat", start: 5, end: 12 },
      { text: "spaghetti", label: "food", start: 60, end: 68 }
    ]
  }
}
```

