---
description: Use the Universal Data Tool in React Applications.
---

# Getting Started with React

## Quick Start: CodeSandbox Example

{% embed url="https://codesandbox.io/s/universal-data-tool-react-usage-example-uerpr?fontsize=14&hidenavigation=1&theme=dark" caption="Example Loading Image Classification Interface" %}

## Installation

```bash
npm install universal-data-tool
```

## Usage

The `<UniversalDataViewer />` component has every interface baked in. Just provide a dataset in the `dataset` prop to view any dataset!

```javascript
import React from "react";
import UniversalDataViewer from "universal-data-tool/components/UniversalDataViewer";

export default function App() {
  return (
    <div className="App">
      <UniversalDataViewer
        // oha is where you put your UDT formatted object
        // Read more about this format here:
        // https://github.com/UniversalDataTool/udt-format
        dataset={{
          interface: { type: "image_classification", labels: ["cat", "dog"] },
          samples: [{ imageUrl: "https://placekitten.com/408/287" }]
        }}
        onExit={(action: "go-to-prev" | "go-to-next" | undefined) => {
          // Called when user hits "Save", "Next", or "Prev"
        }}
        // when data is saved this is called
        onModifySample={(sampleIndex, newSampleData) => {
          // do something
        }}
      />
    </div>
  );
}
```

