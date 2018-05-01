---
layout: post
title:  "HighDimensionalInspector - Configuring the library"
date:   2016-02-06 00:00:00
categories: 
---

{% highlight bash %}
sudo apt-get install cmake
sudo apt-get install qt5-default #Qt
sudo apt-get install gcc-multilib
sudo apt-get install build-essential
sudo apt-get install cmake-gui #if you want to use a gui for the project configuration
{% endhighlight %}

download CUDA
https://developer.nvidia.com/cuda-downloads
sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb 
sudo apt-get update
sudo apt-get install cuda


download flann

cd flann-1.8.4-src/
cmake.
make
sudo make install


