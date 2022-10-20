# SYDE671-ReproducibilityChallenge-2021
Summary
The following reproducibility challenge is based on the paper titled ’Adaptive Convolutions for Structure Aware Style Transfer’ proposed by Prashanth et al., and Disney Research [1]. In essence, the investigated paper introduces Adaptive Convolutions (AdaConv) as an extension of Adaptive Instance Normalization (AdaIN), that focuses on the neural style transfer between images as an artistic application of CNNs, where given a content and style image the goal is to synthesize an output image which has the high level structure of the content image and the artistic style as the style image. As such the outcome of the proposed Adaptive Convolutions framework allows for the simultaneous transfer of both statistical and structural styles.![145637729-f40826c3-7a7c-4352-923e-b24342b4be40]

Code
The code for the AdaConv module and the Kernel predictors was reused from an unofficial imeplementation by REIbars.

The code for AdaIN is also reused from the Torch implementation with python by naoto0804 of the original Torch implementation with lua by the authors.

Listed code repositories are MIT-licensed as open-source for academic research.

Dataset
We used the pretrained weights of the AdaConv framework provided in the open-source repo. The weights were obtained by the author of the AdaConv code using the following datasets.

Content - Click here to go to official COCO dataset website.

Style - Click here to go to official Wiki-Art dataset on Kaggle.

Pretrained weights - Click here to download pretrained-weights to run experiments

Method
By implementing the codes linked above we investigated the results and claims of the paper [1] in three ways:

Outputted visuals of the style latent features across the different layers of the encoder-decoder architecture of AdaConv along with the convolution results
Compared AdaIN and AdaConv results on images and styles in test_images using different techniques (e.g. change in orientation of style image).
Implemented AdaConv to raw content image taken on our phones.
