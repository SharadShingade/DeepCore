---
layout: post
title: Introducing DeepCore
author: Joe White
author_title: Software Development Manager, DeepCore
---

If you've come this far, you're probably wondering what DeepCore is and what it does, maybe even what it can do for **you**.

Put simply, DeepCore is a way to abstract all the fiddly bits of machine learning and neural networks away from the user, making it easier to use these different frameworks and APIs.  We want to make it simple to do machine learning and object detection, especially in a geospatial context.  After all, spatial stuff is important.

The whole concept behind the DeepCore framework is to give the developer a way to use machine learning without having to be a domain expert on machine learning. We're building blocks that fit together in new and interesting ways, allowing the user to take them and make whatever masterpiece they want.  That's the good stuff.

It's all written in modern C++, with additional language bindings upcoming.  We know there is a big data science world out there in Python, and we **DO** intend to bring DeepCore to Python. Our current implementation only includes [Caffe](https://http://caffe.berkeleyvision.org), but additional frameworks are currently being added like [Dlib](https://dlib.net) and [TensorFlow](https://www.tensorflow.org).  If you've got some features you want, feel free to let us know on our [Issues](https://github.com/DigitalGlobe/DeepCore/issues) page.

There are a couple of sample projects using DeepCore out there in Github.  First, there's our [gbdxm packaging library](https://digitalglobe.github.io/DeepCore/index.html#three).  When we load machine learning models for processing and classification, it's more convenient to use a single package.  To that end, we made the packager. It makes sharing models much more convenient by packaging them up as a single file.  It also creates metadata to be able to determine which model would be best for a given job, like geographic bounding box, image size used for training,etc.
 

Next is [OpenSpaceNet](https://digitalglobe.github.io/DeepCore/index.html#four).  This sample uses DeepCore to download web service map tiles or load a local image, run a detection cycle with a model, then output the results as a geospatial vector file format or database.  This is more of a full featured way to get DigitalGlobe imagery from our services, run a detector on it, and get results that can be visualized  in a desktop GIS application.  The user is responsible for getting their own credentials for each service, though.
 
The services are:
 * [DigitalGlobe Services](https://services.digitalglobe.com)
 * [DigitalGlobe Web Maps API](https://platform.digitalglobe.com/maps-api/)
 
Please visit the service websites to sign up and start making use of DigitalGlobe imagery!

Thanks for checking out DeepCore,

Joe White

![alt-text]({{ site.baseurl }}/images/banner2.png)
