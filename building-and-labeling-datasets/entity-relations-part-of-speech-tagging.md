---
description: >-
  Named Entity Linking (PoS tagging) with the Universal Data Tool. Draw
  relationships between words or phrases within text.
---

# Entity Relations / Part of Speech Tagging

## Setup the Dataset

Navigate to [udt.dev](https://udt.dev) and click "New File"

![Click &quot;New File&quot; on udt.dev](../.gitbook/assets/image%20%2815%29.png)

Then select the Text Entity Relations button from the `Setup > Data Type` page.

![Select Text Relations when choosing an interface](../.gitbook/assets/image%20%2822%29.png)

You can now configure the interface you'd like for you Text Entity Relations dataset by adding any labels you'd like to display per sample.

![Text Entity Relation Configuration](../.gitbook/assets/image%20%2871%29.png)

## Import Data

You can use any of the following methods to import text data.

* [Import Text Snippets](../importing-data/import-text-snippets.md)
* [Import from CSV or JSON](../importing-data/import-from-csv-or-json.md)

## Label your Data \(with friends!\)

Go to the `Label` tab to begin labeling data. See the [Collaborative Labeling Guide](../collaborative-labeling.md) to label with friends or a team of your labelers.

![Example of Text Entity Relations labeling](../.gitbook/assets/image%20%2856%29.png)

## Export and Use

The easiest way to use a Entity Relations dataset is using the JSON format. Use the "Download JSON" button at the top when you're done labeling and check out the [Text Entity Relations JSON Specification](https://github.com/UniversalDataTool/udt-format/blob/master/interfaces/text_entity_relations.md).

Here's what a JSON sample looks like in the resultant dataset:

```javascript
{
  "document": "This strainer makes a great hat, I'll wear it while I serve spaghetti!",
  "annotation": {
    "entities": [
      {
        "text": "strainer",
        "label": "hat",
        "start": 5,
        "end": 13,
        "textId": "id1"
      },
      {
        "text": "spaghetti",
        "label": "food",
        "start": 60,
        "end": 69,
        "textId": "id2"
      },
      {
        "text": "I'll",
        "start": 33,
        "end": 37,
        "textId": "id3"
      },
      {
        "text": "wear",
        "start": 38,
        "end": 42,
        "textId": "id4"
      }
    ],
    "relations": [
      {
        "from": "id3",
        "to": "id4",
        "label": "subject-doing"
      }
    ]
  }
}
```

