# What is the .udt.csv format?

The .udt.csv format is another representation of the .udt.json object that allows easier viewing and editing of data in spreadsheet software. 

![A udt.csv file has easy to understand columns!](.gitbook/assets/image.png)

{% hint style="info" %}
[Check out this example .udt.csv file!](https://github.com/UniversalDataTool/udt-format/blob/master/SAMPLE.udt.csv)
{% endhint %}

{% hint style="info" %}
The UDT CSV format is capable of specifying all the same things as the UDT JSON format, but the UDT JSON format is the "canonical form" because the .udt.csv files are very flexible, and can be written in different but equivalent ways.
{% endhint %}

{% hint style="info" %}
UDT CSV files are generating by converting the JSON format into a CSV using [JSON as CSV \(JAC\)](https://github.com/UniversalDataTool/jac-format). They can be converted back to JSON using the [jac-format npm module](https://www.npmjs.com/package/jac-format) or [jac\_format pip module](https://pypi.org/project/jac-format/).
{% endhint %}

The UDT CSV format is really easy to use with libraries like [pandas](https://pandas.pydata.org/).

