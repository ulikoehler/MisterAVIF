# MisterAVIF

Find the correct AVIF compression settings for your images by visually comparing images

Give `MisterAVIF` an image and he will compress in from quality 5 to 100 in steps of 5.

It will also extract some small sections of the image to compare the compression quality visually, which is helpful for high-resolution images.

## Example

As an example, take this photo of Nuremberg, Germany(made by me, open-sourced under CC0):

![Example image of Nuremberg, Germany](./examples/Nuremberg.jpg)

In the original compression from the camera, it's `3.2MB` large.

Let's use `MisterAVIF` to compress it to different qualities and compare the results.

```bash
misteravif examples/Nuremberg.jpg
```

`MisterAVIF` will now take its time to generate all the different compression levels. For this image and on my machine, this takes about `1:34` minutes (yeah, AVIF encoding is slow, but it's equally effective).

It will create a director `examples/Nuremberg` with the following files:

```
-Filesizes.png
Original.jpg
q05.avif
q100.avif
q10.avif
q15.avif
q20.avif
q25.avif
q30.avif
q35.avif
q40.avif
q45.avif
q50.avif
q55.avif
q60.avif
q65.avif
q70.avif
q75.avif
q80.avif
q85.avif
q90.avif
q95.avif
Section a1.png
Section a2.png
Section a3.png
Section b1.png
Section b2.png
Section b3.png
Section c1.png
Section c2.png
Section c3.png
```

The `Original.jpg` is the original image, and the `qXX.avif` files are the compressed images with different qualities. You can use them to check out the complete image with a given quality level.

For example, checkout the `q05.avif` file, which is the lowest quality setting being generated.

![Example image of Nuremberg, Germany, compressed to 5% quality using AVIF](./examples/Nuremberg-q05.avif)


What's most interesting is 