---
description: Use the Universal Data Tool directly within a Jupyter Notebook
---

# Jupyter Notebook Integration

## Installation

To get started, we'll need to install the [Universal Data Tool python module](https://pypi.org/project/universaldatatool/).

```bash
pip install universaldatatool
```

## Creating a Dataset

Creating datasets inside python is really easy!

```python
import universaldatatool as udt

ds = udt.Dataset(
    type="image_segmentation",
    image_paths=["/path/to/birds/good_bird.jpg","/path/to/birds/bird2.jpg"],
    labels=["good bird", "bad bird"]
)

# Opens dataset directly in jupyter notebook
ds.open()
```

![The Universal Data Tool will open inside of your Jupyter Notebook](../.gitbook/assets/image%20%2814%29.png)

## Loading a udt.json or udt.csv file

```python
import universaldatatool as udt

ds = udt.load()

# Opens dataset directly in jupyter notebook
ds.open()
```

## This page isn't ready!

We're still waiting on a contributor to write this page. If you'd like to help out, click the Edit on Github button above!

