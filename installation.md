# Installation

## Usage on Web

Just go to [universaldatatool.com/app](https://universaldatatool.com/app)!

## Using on Desktop \(Windows, Mac, Linux\)

You can download the latest releases of the Universal Data Tool from the [Github Releases page](https://github.com/UniversalDataTool/universal-data-tool/releases).

{% hint style="info" %}
Our Windows Desktop application needs contributors! If you run into any issues, or better yet manage to resolve them, [send us a contribution!](https://github.com/UniversalDataTool/universal-data-tool/tree/master/CONTRIBUTING.md)
{% endhint %}

## Using with Python or Jupyter Notebook

If you use [Fast.ai](machine-learning/fastai/) or [Tensorflow](), [Pytorch](), brat etc. look at the respective guides in the Machine Learning section of these docs. 

```python
import universaldatatool as udt

ds = udt.Dataset(
    interface="image_classification",
    image_urls=["https://example.com/image1.png"],
    labels=["cat", "dog"]
)

ds.to_json() # Outputs .udt.json

udt.open() # Opens the Universal Data Tool in Jupyter Notebooks
```

You can do much more! Check out the [Getting Started with Python](machine-learning/jupyter-notebooks.md) for more details!

## Using with React or Embedded on Webpage

Check out the guide for [Getting Started with React](integrate-with-any-web-page/getting-started-with-react.md) or [Integrate the Javascript Library](integrate-with-any-web-page/integrate-with-the-javascript-library.md).

{% hint style="info" %}
I recommend trying out the web tool before integrating. For many use cases, you can avoid the integration all together just by [using the online tool](https://universaldatatool.com/app)!
{% endhint %}

```
$ give me super-powers
```



