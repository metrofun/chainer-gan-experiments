# Chainer-GANs

Various GANs with Chainer

### List
* DCGAN: [Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/abs/1511.06434)
* LSGAN: [Least Squares Generative Adversarial Networks](https://arxiv.org/abs/1611.04076)
* WGAN: [Wasserstein GAN](https://arxiv.org/abs/1701.07875)
* WGAN-GP: [Improved Training of Wasserstein GANs](https://arxiv.org/abs/1704.00028)
* DRAGAN: [How to Train Your DRAGAN](https://arxiv.org/abs/1705.07215)
* [WIP]Alpha-GAN: [Variational Approaches for Auto-Encoding Generative Adversarial Networks](https://arxiv.org/abs/1706.04987)


### Gradient Penalty

Most of recent GANs (WGAN-GP, CramerGAN, DRAGAN) contains the gradient norm regularization, this has been proved as a way to stablize GAN training.

The current version of Chainer do not support high order derivatives, a solution is to mannually implement the backward procedure with auto-differentiable chainer.functions. (Refer the WGAN-GP codes for the details.)

* L.Linear, L.Convolution2D, L.Deconvolution2D, F.leaky_relu, F.relu, F.sigmoid, F.tanh, L.LayerNormalization is implemented.
* Some GAN papers suggest to use LayerNormalization instead on BatchNormalization in the discriminator in the case of gradient penalty. 


**Special thanks to [mattya](https://github.com/mattya) for the idea and reference codes.**


