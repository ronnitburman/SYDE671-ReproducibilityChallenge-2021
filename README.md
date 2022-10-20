# ReproducibilityChallenge2021
SYDE 671 - Final Report and Code 


## Adaptive Convolutions for Structure-Aware Style Transfer 

### Summary 

The following reproducibility challenge is based on the paper titled ’Adaptive Convolutions for Structure Aware Style
Transfer’ proposed by Prashanth et al., and Disney Research [1]. In essence, the investigated paper introduces Adaptive
Convolutions (AdaConv) as an extension of Adaptive Instance Normalization (AdaIN), that focuses on the neural
style transfer between images as an artistic application of CNNs, where given a content and style image the goal is to
synthesize an output image which has the high level structure of the content image and the artistic style as the style
image. As such the outcome of the proposed Adaptive Convolutions framework allows for the simultaneous transfer of
both statistical and structural styles.![145637729-f40826c3-7a7c-4352-923e-b24342b4be40]

### Code 

The code for the [AdaConv module ](https://github.com/RElbers/ada-conv-pytorch/blob/master/lib/adaconv/adaconv.py/) and the [Kernel predictors](https://github.com/RElbers/ada-conv-pytorch/blob/master/lib/adaconv/kernel_predictor.py/) was reused from an unofficial imeplementation by [REIbars](https://github.com/RElbers/ada-conv-pytorch).


The code for AdaIN is also reused from the [Torch implementation with python](https://github.com/naoto0804/pytorch-AdaIN) by [naoto0804](https://github.com/naoto0804/pytorch-AdaIN) of the original [Torch implementation with lua](https://github.com/xunhuang1995/AdaIN-style) by the [authors](https://github.com/xunhuang1995/AdaIN-style). 

Listed code repositories are MIT-licensed as open-source for academic research. 

### Dataset 

We used the pretrained weights of the AdaConv framework provided in the open-source repo. The weights were obtained by the author of the 
AdaConv code using the following datasets. 

Content - Click [here](https://cocodataset.org/#home) to go to official COCO dataset website. 

Style - Click [here](https://www.kaggle.com/antoinegruson/-wikiart-all-images-120k-link) to go to official Wiki-Art dataset on Kaggle.

Pretrained weights - Click [here](https://drive.google.com/file/d/17h-Hd08n-f_5D8cDV08dpB_-W1cs5jbt/view?usp=sharing) to download pretrained-weights to run experiments 

### Method

By implementing the codes linked above we investigated the results and claims of the paper [1] in three ways: 
1. Outputted visuals of the style latent features across the different layers of the encoder-decoder architecture of AdaConv along with the convolution results
3. Compared AdaIN and AdaConv results on images and styles in test_images using different techniques (e.g. change in orientation of style image). 
4. Implemented AdaConv to raw content image taken on our phones. 
