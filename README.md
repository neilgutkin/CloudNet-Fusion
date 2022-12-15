# Deep Fusion Architectures for Cloud Masking
#### Authors: Neil Gutkin, Daniel Hajialigol

Experimenting with deep fusion architectures for cloud masking, with the early fusion CloudNet [1] approach as a baseline.
The CloudNet approach is re-written in Torch, then used in middle-fusion and late-fusion schemes.

In middle fusion, two separate encoders are used for the RGB and NIR input images. The NIR branch shares information with the RGB
branch during the encoding process through element-wise addition. The generated feature representation is then used as input to
a shared decoder. 

In late fusion, there are two separate encoders and decoders, with the fusion happening at the very end, in a sort-of ensemble
learning approach to the problem.

[1] S. Mohajerani and P. Saeedi, Cloud-net: An end-to-end cloud detection algorithm for landsat 8 imagery,
IGARSS 2019 - 2019 IEEE International Geoscience and Remote Sensing Symposium, (2019)
