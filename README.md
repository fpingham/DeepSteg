# DeepSteg
## Implementation of Hidding Images in Plain Sight: Deep Steganography in Pytorch

### History

Steganography is the art of hidding a piece of information in a carrier which, at first glance, carries another piece of information. According to [Wikipedia](https://en.wikipedia.org/wiki/Steganography), the first examples of steganography date back to 440BC (as per Herodotus in Histories) when Hisitaeus sent a message to Aristagoras by shaving the head of a servant, writting a message on his head and ordering him to have his head shaved only upon arrival to transmit the message. The other example is Demaratus who warned about an incoming attack from Xerxes to Greece by hidding it in a wax tablet, between the wood and the wax.

### Abstract

Steganography is the practice of concealing a secret message within another,
ordinary, message. Commonly, steganography is used to unobtrusively hide a small
message within the noisy regions of a larger image. In this study, we attempt
to place a full size color image within another image of the same size. Deep
neural networks are simultaneously trained to create the hiding and revealing
processes and are designed to specifically work as a pair. The system is trained on
images drawn randomly from the ImageNet database, and works well on natural
images from a wide variety of sources. Beyond demonstrating the successful
application of deep learning to hiding images, we carefully examine how the result
is achieved and explore extensions. Unlike many popular steganographic methods
that encode the secret message within the least significant bits of the carrier image,
our approach compresses and distributes the secret image’s representation across
all of the available bits.

