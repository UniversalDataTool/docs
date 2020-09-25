---
description: 'Pandas gives you a nice way to view, filter and convert UDT datasets.'
---

# Import Datasets into Pandas

## Exporting UDT Dataset as CSV

You can export any UDT dataset into a CSV file using the download button at the top of the page.

![](../.gitbook/assets/image%20%2817%29.png)

## Importing udt.csv into Pandas

## Import CSV Into Pandas Dataframe

We can begin by importing the pandas, and our udt.csv file. 

```python
import pandas as pd

url_or_filepath_to_csv = "https://raw.githubusercontent.com/UniversalDataTool/udt-dataset-cats-and-dogs/master/coco_dogs_and_cats.udt.csv"
udt_csv = pd.read_csv(url_or_filepath_to_csv)
```

{% hint style="info" %}
You can use the udt.json format too, tables are just a nice way to visualize the data!
{% endhint %}

If you view the udt\_csv object, you should now see a breakdown of your CSV, ready to be imported!

![coco\_dogs\_and\_cats.udt.csv](../.gitbook/assets/image%20%2812%29.png)

## Downloading Images

UDT Datasets just have links to images, so we'll need to download the actual images. Check out the [fast.ai Image classification tutorial](fastai/import-datasets-for-fast.ai-image-classification.md), where we show how to easily download images using the fast.ai download\_images function.

