python-rescale
==============

A simple tool to resize and crop an image

```
rescale(image, size, mode=None)
```

 * image: a PIL image object
 * size: a 2-tuple (width, height); at least one must be specified
 * mode: `CROP_TL` or `CROP_BR`

If no height or no width is specified, the mode won't be taken into account, and the image will just be resized.

If both width and height are provided, and the mode is set top `CROP_TL` or `CROP_BR`, the image will be cropped to the given size using the given mode. Note that the crop is made after the image as been resized (well not exactly, but the result is the same) to preserve as much as possible the content of the image.

The resize is made so that the original ratio is preserved.

The `CROP_TL` mode will keep the top left or the image, while `CROP_BR` will keep the bottom right of it.
