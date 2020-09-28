---
description: FAQ for the Universal Data Tool
---

# Frequently Asked Questions

## Why are fractional coordinates used instead of pixel coordinates in the Universal Data Tool?

Pixel coordinates can often be helpful for drawing or extraction part of an image. However, fractional coordinates, meaning coordinates in the range `[0,1]` are used for representing the location on an image in the UDT for the following reasons:

* It is resilient to image resizing/changes to size in the underlying image source
* Most images are rescaled prior to being put into a machine learning model, at which point a pixel coordinate transformation would be necessary and cumbersome
* It better supports "massive" image scenarios, such as maps or microscopic slides, that have variable pixel accuracy

If you need to convert UDT fractional coordinates into pixel coordinates, you can do it quickly with[ udt-to-image-position](https://github.com/UniversalDataTool/udt-to-image-position).

