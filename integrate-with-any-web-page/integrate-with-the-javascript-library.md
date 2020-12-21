---
description: >-
  Use the Universal Data Tool in any javascript application using a <script />
  import tage.
---

# Integrate with the Javascript Library

## Quick Start: UDT in Static HTML Page

{% embed url="https://codesandbox.io/s/universal-data-tool-in-any-web-page-s8mh6" %}

## Installation

Put a script tag at the top of your page importing the Universal Data Tool "vanilla" library.

{% hint style="info" %}
The vanilla library bundles all the Universal Data Tool dependencies together into a single file, making it easy to use anywhere!
{% endhint %}

```markup
<script
    type="application/javascript"
    src="https://unpkg.com/universal-data-tool@0.13.2/vanilla.js"
></script>
```

## Usage

Add a container element to your body. Then call `window.UniversalDataTool.open` to open the UDT in your element.

```markup
<body>
  <div id="udt"></div>
  <script type="application/javascript">
    window.UniversalDataTool.open({
      container: document.getElementById("udt"),
      
      // Your UDT dataset
      // https://github.com/UniversalDataTool/udt-format
      udt: {
        interface: {
          type: "image_classification",
          labels: ["A", "B"]
        },
        samples: [
          {
            imageUrl: "https://placekitten.com/408/287"
          }
        ]
      },
      
      // Called when sample is saved
      onSaveSample: (index, sample) => {
        console.log(index, sample);
      }
    });
  </script>
</body>
```

