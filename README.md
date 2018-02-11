# DeepSteg
## Implementation of _Hidding Images in Plain Sight: Deep Steganography_ in Pytorch

This is an unofficial implementation in Pytorch of _Hidding Images in Plain Sight: Deep Steganography_ **by Shumeet Baluja (NIPS 2017)** for the Global NIPS Paper Implementation Challenge. Here is the [original paper](https://papers.nips.cc/paper/6802-hiding-images-in-plain-sight-deep-steganography).

### History

Steganography is the art of hidding a piece of information in a carrier which, at first glance, carries another piece of information. According to [Wikipedia](https://en.wikipedia.org/wiki/Steganography), the first examples of steganography date back to 440BC (as per Herodotus in Histories) when Hisitaeus sent a message to Aristagoras by shaving the head of a servant, writting a message on his head and ordering him to have his head shaved only upon arrival to transmit the message. The other example is Demaratus who warned about an incoming attack from Xerxes to Greece by hidding it in a wax tablet, between the wood and the wax.

### Abstract of the paper

> Steganography is the practice of concealing a secret message within another,
> ordinary, message. Commonly, steganography is used to unobtrusively hide a small
> message within the noisy regions of a larger image. In this study, we attempt
> to place a full size color image within another image of the same size. Deep
> neural networks are simultaneously trained to create the hiding and revealing
> processes and are designed to specifically work as a pair. The system is trained on
> images drawn randomly from the ImageNet database, and works well on natural
> images from a wide variety of sources. Beyond demonstrating the successful
> application of deep learning to hiding images, we carefully examine how the result
> is achieved and explore extensions. Unlike many popular steganographic methods
> that encode the secret message within the least significant bits of the carrier image,
> our approach compresses and distributes the secret image’s representation across
> all of the available bits.

### Idea
The architecture includes a Prep Network, a Hidding Network and a Reveal Network. Input is secret and cover images and output is hidden image (output of Hidding Network) and output image (output of Reveal Network).

![Idea](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/DeepStegIdea2.png)

Source: Hidding Images in Plain Sight: Deep Steganography, Shumeet Baluja, 2017

### Errors
Error Term 1 (difference between cover and hidding image) is backprops only through first two networks while Error Term 2 (differnce between secret and output image) backprops through all four networks.

![Errors](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/DeepStegIdea.png)

Source: Hidding Images in Plain Sight: Deep Steganography, Shumeet Baluja, 2017

### Results

I finally used a beta of 2 instead of 0.25-0.75 as the paper suggests. The following results are, in order: secret image, output image, cover image and hidden image. These results are after the full run of one epoch.

![Example 4](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/results5.png)

![Example 3](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/results4.png)

![Example 2](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/results3.png)

![Example 1](https://github.com/lesscomfortable/DeepSteg/blob/master/Images/results2.png)
