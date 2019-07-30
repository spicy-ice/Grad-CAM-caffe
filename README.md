# Grad-CAM-caffe
Feature map visualization

http://sandaw89.blogspot.com/2017/08/gradcam-implementation-in-pycaffe.html  (Need to over the wall)


To implement Grad-CAM we need gradients of the layer just before the softmax layer with respect to a convolution layer, preferably the last convolution layer. To achieve this you have to modify the deploy.prototxt file. You just have to remove the softmax layer and add following line just after the model name.

```
force_backward: true
```
