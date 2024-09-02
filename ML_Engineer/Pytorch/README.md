# ML Engineering Interview: Rust

## The Problem

We would like you to write an img2img algorithm that creates a neural network that can automatically derive a **Sobel Filter Kernel** based on a set of input and output images. The output images are simply the input images with a sobel filter applied.

You should make the decision of what kind of network to use, how to structure the layers, etc. Most architectures will work as the network is likely to very quickly converge, but keep in mind what goal you are optimizing for.

**NOTE:** if your model architecture is very deep or you are borrowing an off-the-shelf model, you are likely not thinking about this problem in the right way.

## Some questions

1. What if the image is really large or not of a standard size?
2. What should occur at the edges of the image?
3. Are you using a fully convolutional architecture?
4. Are there optimizations built into your framework of choice (e.g. Pytorch) that can make this fast?
5. What if you wanted to optimize specifically for model size?
6. How do you know when training is complete?
7. What is the benefit of a deeper model in this case? When might there be a benefit for a deeper model (not with a sobel kernel but generally when thinking about image to image transformations)?

## What is a Sobel Filter?

[Wikipedia](https://en.wikipedia.org/wiki/Sobel_operator) has everything you need to know to answer this question.

## What libraries should I use?

Pytorch is our favorite, but it's up to you! For a Sobel filter that you can use to construct the training set, there are many options (including just doing the convolution in torch), but there's the `cv2.Sobel` filter pre-made.

## Where can I get a training dataset?

This is up to you! There are lots of easy dataset libraries out there. Often these libraries allow you to write in transforms or other easy operators. You can always just download COCO or ImageNet. There's of course [img2dataset](https://github.com/rom1504/img2dataset)

## Extra credit question

Now generalize your algorithm so that it can learn any arbitrary image kernel-based filter. You could test this by randomizing the kernel. What are the limitations of this?
