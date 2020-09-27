---
description: Use multiple UDT interfaces together with a Composite Interface.
---

# Composite Interfaces

## What is a Composite Interface?

A composite interface is an interface that contains other interfaces within in. It's very helpful if you're doing multiple operations on an image. For example, you might need to do some data entry on an image, such as doing Optical Character Recognition.

## Setup the Dataset

Select "Composite" from `Setup > Data Type`, then select Configure to create additional interfaces, and configure each one individually.

![](../.gitbook/assets/image%20%2864%29.png)



## Labeling Composite Interfaces

When labeling a composite interface, you'll be prompted to select any of the sub-interfaces on each sample.

![Select each sub-interface when labeling to add data for that sample](../.gitbook/assets/image%20%2866%29.png)

## Exporting JSON

When exporting a composite interface, it's best to use the JSON format. Check out the [Composite Interface JSON Format ](https://github.com/UniversalDataTool/udt-format/blob/master/interfaces/composite.md)Specification.

The resultant JSON for each sample looks like this:

```javascript
{
  /* ... same information as sample, e.g. imageUrl ... */

  // Expected annotation
  "annotation": {
    // Each key is a fieldName, the annotation is the annotation from that interface
    "some_field_name": {/*... whatever annotation goes with the interface defined for this field ...*/}
  }
}
```



