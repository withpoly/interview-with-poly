# Platform Engineering Interview: Ray

## The Problem

We would like you to implement a distributed Stable Diffusion pipeline using Ray. You are not expected to actually implement the Stable Diffusion algorithm/model, but just to use a standard off-the-shelf implementation such as HuggingFace. You are also not required to use the latest model, you can use something much simpler (like V1.5). However, you must implement the pipeline such that the different stages of the pipeline are distributed, i.e. that the three primary steps happen in a distributed fashion (on different Ray workers/actors/functions):

1. Text encoding
2. Latent Generation
3. Image Decoding from Latent

## Questions

1. How would you optimize this pipeline for speed?
2. When would you use batching, and where? What are the trade-offs?
3. Is a distributed implementation faster than a fully local implementation? Why, or when?
4. What are some different architectures for the distributed pipeline? Why did you choose the one you went with?
5. How would you use the Ray concept of Remote Objects to your advantage?

## Resources to solve this problem

You are totally free to use any resources you can imagine, including tutorials you find online, etc. If you can find a tutorial online that has this word-for-word implemented, feel free to take that as a starting point and improve upon it. You can use the documentation for HuggingFace, Ray, and anything else. You may use AI-assisted tools or code editing, though we would highly advise that you focus mostly on the conceptual aspects of the problem rather than docstrings, etc. Here are some basic places to get started:

* [Stable Diffusion 1.5](https://huggingface.co/runwayml/stable-diffusion-v1-5)
* [Intro to Ray](https://docs.ray.io/en/latest/ray-overview/index.html)

## What are we looking for?

Our goal is to see if you understand the basic distributed capabilities of Ray. We are not looking to find the fastest implementation possible. You may focus on a CPU-only inference pipeline (you can use a smaller resolution such as 256x256 to do so if you choose). You will want to explore how the stages of the pipeline are organized, and how you would use different pieces of the Ray stack to solve this problem. The two main building blocks of Ray are *tasks* and *actors*. You will need to determine which of these to use and how.

## What is Stable Diffusion?

Stable Diffusion is a diffusion-based model for genetating images. The model notably generates images in a "latent" representation to speed up inference.

## What is Ray?

Ray is a distributed framework for Python programming that lets you use fuction decorators to create distributed, remote executing methods.
