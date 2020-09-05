# What is the .udt.json format?

The UDT JSON format is an [open-source format](https://github.com/UniversalDataTool/udt-format) for specifying human annotation tasks. For example, you might use the .udt.json format to store the labels and specification for transcribing audio or labeling images. 

{% hint style="info" %}
The UDT JSON format can be [converted to and from an equivalent CSV format](what-is-the-.udt.csv-format.md) easily.
{% endhint %}

The basic structure of a UDT JSON file is this:

```javascript
{
    "interface": {
        "type": "<some_interface>"
        // ... more interface details
    },
    "samples": [
        { /* sample json object */ },
        // ...
    ]
}
```

Here's an example for an [image segmentation](building-and-labeling-datasets/image-segmentation.md) dataset...

```javascript
{
  "interface": {
    "type": "image_segmentation",
    "labels": [
      {
        "id": "cat",
        "description": "Feline Mammal"
      },
      {
        "id": "dog",
        "description": "Canine Mammal"
      }
    ],
    "regionTypesAllowed": ["bounding-box"],
    "multipleRegions": true
  },
  "samples": [
    {
      "imageUrl": "https://media.gettyimages.com/photos/dog-and-cat-picture-id151350785"
    },
    {
      "imageUrl": "https://media.gettyimages.com/photos/guess-who-rules-the-roost-in-that-house-picture-id500927195"
    },
    {
      "imageUrl": "https://media.gettyimages.com/photos/she-simply-loves-animals-picture-id499806311"
    }
  ]
}
```

### Principles

The principles that drive the UDT format are...

* **Complete Specificity** such that no additional documents or conversations are required to perform the task.
* **Simplicity and Human Readability** so that datasets can be easily examined in the JSON format and understood
* **Specificity** such that no additional documents or conversations are required to start labeling

