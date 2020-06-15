# HiDT 
> Recration of the High-Resolution Daytime Translation without Domain Labels paper in PyTorch. This is an unnoficial implementation. For the original work please see <a href='http://openaccess.thecvf.com/content_CVPR_2020/papers/Anokhin_High-Resolution_Daytime_Translation_Without_Domain_Labels_CVPR_2020_paper.pdf'>here</a>


## Background on HiDT

Previous unsupervised image to image translation architectures such as UNIT, MUNIT and FuNIT have progressively gotten better at working with more general datasets. UNIT eliminated the requirement of having paired labels of data in two seperate domains by creating a latent space assumption and attempting to create models to map to and from this space from each domain. MUNIT expanded on this work by allowing images from more than 2 domain be translated. More recently, FuNIT expanded this further by allowing to train on brand new classes of a only a few examples, but still requires large amounts domain labels for training. The natural progression in these models then becomes, is there a way to train on any random groups of pictures, without any labelling which is exactly what HiDT aims to do.

# Specifics

Specifically, HiDT presents 3 contributions:

<ol>
<li> Creating a model to train on a large amount of unlabelled and unalliigned (no inter-domain matching) images 
    <img src="model.png">
    Code for this can be found in "Training"
<li> Generator for image to image translation combining AdaINs and skip connections
    <img src="adaptiveunet.png">
    Code for this can be found in "Adaptive Unet"
<li> A new enhancement method for training translation models on high resolution images
<ol>

## TODO

<ul>
    <li> Implement enhancement scheme postprocessing for high res translations
    <li> Test schedulers on discriminator/generator training split
    <li> Test custom segmentation model using encoder features
    <li> Benchmark half precision train time
<ul>
