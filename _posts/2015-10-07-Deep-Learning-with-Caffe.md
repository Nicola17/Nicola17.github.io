---
layout: post
title: Deep Learning with Caffe
date: '2015-10-07T00:00:00.000+02:00'
author: Nicola Pezzotti
tags:
- Deep Learning
- Caffe
- Python
- AI
- CUDA
---

I want to play around with some [Deep Learning][1] algorithms.
After some readings, I decided to do some experiments with [Caffe][2]. 
*Caffe is a deep learning framework made with expression, speed, and modularity in mind.*

It is fairly easy to start using some [Deep Neural Nets][1] with Caffe. 
There are plenty of [pre-trained model][5] that you can use right away to do some experiments.
In this post I want to share my experience with Caffe under Ubuntu 14.04 LTS.
During the installation I mainly followed [this guide](http://caffe.berkeleyvision.org/install_apt.html).


Installation
--------------------

First, I installed some dependencies.
{% highlight bash %}
sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev 
sudo apt-get install libopencv-dev libhdf5-serial-dev protobuf-compiler
sudo apt-get install --no-install-recommends libboost-all-dev
sudo apt-get install cuda python-dev libatlas-dev libatlas-base-dev
sudo apt-get install libgflags-dev libgoogle-glog-dev liblmdb-dev
sudo pip install numpy
{% endhighlight %}

Then, I cloned Caffe from the [official repository][4] and I compiled it.
{% highlight bash %}
cd caffe
mkdir build
cd build
cmake ..
make
{% endhighlight %}

Finally I had to install some packages required by the python module...
{% highlight bash %}
pip install scipy
pip install scikit-image
pip install protobuf
pip install pyyaml
{% endhighlight %}

... and I added the caffe's python folder in the environment variable PYTHONPATH.
{% highlight bash %}
export PYTHONPATH=/path/to/caffe/python/
{% endhighlight %}

Now we are ready to go... let's do some test!

Test
------------------

I started usign [this tutorial][6].
The goal is to have a feature extractor that is working using the pre-trained model from [Krizhevsky et al.][8] that is working on the  [ImageNet][7] dataset.
We need to download the model and the labels first.

{% highlight bash %}
cd /path/to/caffe
#download the model
./scripts/download_model_binary.py ./models/bvlc_reference_caffenet
#download the labels
./data/ilsvrc12/get_ilsvrc_aux.sh

cd /path/to/sandbox
mkdir images
{% endhighlight %}


I downloaded few pictures and added to the images folder.

<img src="{{ site.baseurl }}/images/wine.jpg" height="150">
<img src="{{ site.baseurl }}/images/dog.jpg" height="150">
<img src="{{ site.baseurl }}/images/old_camera.jpg" height="150">


And with the following script I run the feature-extraction/classification. 
The script is really simple, however I'm planning to write ASAP a script that can deal with tons of images.

{% highlight python %}
import numpy as np
import caffe

caffe_root = '/path/to/caffe/'  

caffe.set_mode_gpu()
#caffe.set_mode_cpu() if you don't have an NVIDIA card

net = caffe.Net(caffe_root + 'models/bvlc_reference_caffenet/deploy.prototxt',
                caffe_root + 'models/bvlc_reference_caffenet/bvlc_reference_caffenet.caffemodel',
                caffe.TEST)

# input preprocessing: 'data' is the name of the input blob == net.inputs[0]
transformer = caffe.io.Transformer({'data': net.blobs['data'].data.shape})
transformer.set_transpose('data', (2,0,1))
transformer.set_mean('data', np.load(caffe_root + 'python/caffe/imagenet/ilsvrc_2012_mean.npy').mean(1).mean(1)) # mean pixel
transformer.set_raw_scale('data', 255)  # the reference model operates on images in [0,255] range instead of [0,1]
transformer.set_channel_swap('data', (2,1,0))  # the reference model has channels in BGR order instead of RGB
imagenet_labels_filename = caffe_root + 'data/ilsvrc12/synset_words.txt'
labels = np.loadtxt(imagenet_labels_filename, str, delimiter='\t')
net.blobs['data'].reshape(50,3,227,227)

net.blobs['data'].data[...] = transformer.preprocess('data', caffe.io.load_image('./images/wine.jpg'))
out = net.forward()
top_k = net.blobs['prob'].data[0].flatten().argsort()[-1:-6:-1]
print labels[top_k]

net.blobs['data'].data[...] = transformer.preprocess('data', caffe.io.load_image('./images/dog.jpg'))
out = net.forward()
top_k = net.blobs['prob'].data[0].flatten().argsort()[-1:-6:-1]
print labels[top_k]

net.blobs['data'].data[...] = transformer.preprocess('data', caffe.io.load_image('./images/old_camera.jpg'))
out = net.forward()
top_k = net.blobs['prob'].data[0].flatten().argsort()[-1:-6:-1]
print labels[top_k]


{% endhighlight %}

And the results is the following, quite impressive ;)

{% highlight bash %}
['n07892512 red wine' 'n04591713 wine bottle' 'n02823428 beer bottle'
 'n04579145 whiskey jug' 'n03690938 lotion']
['n02099601 golden retriever'
 'n02102318 cocker spaniel, English cocker spaniel, cocker'
 'n02108551 Tibetan mastiff' 'n02102480 Sussex spaniel'
 'n02100877 Irish setter, red setter']
['n04069434 reflex camera'
 'n03976467 Polaroid camera, Polaroid Land camera' 'n04009552 projector'
 'n03843555 oil filter' 'n03666591 lighter, light, igniter, ignitor']
{% endhighlight %}



[1]: https://en.wikipedia.org/wiki/Deep_learning
[2]: http://caffe.berkeleyvision.org/
[4]: https://github.com/BVLC/caffe
[5]: https://github.com/BVLC/caffe/wiki/Model-Zoo
[6]: http://nbviewer.ipython.org/github/BVLC/caffe/blob/master/examples/00-classification.ipynb
[7]: http://www.image-net.org/
[8]: http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks
