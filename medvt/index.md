---
layout: default
title: <h2>MED-VT Multiscale Encoder Decoder Video Transformer(CVPR'23).</h2>
description: <a href="https://rkyuca.github.io"><div class="author">Rezaul Karim,</div></a>&nbsp;<a href="https://joehezhao.github.io/"><div class="author">He Zhao,</div></a>&nbsp;<a href="https://lassonde.yorku.ca/users/wildes"><div class="author">Richard P. Wildes,</div></a>&nbsp;<a href="https://msiam.github.io/homepage/"><div class="author"><div class="author">Mennatullah Siam</div></a></div><br><a href=""><div class="hbtn">Paper</div></a>&nbsp;<a href=""><div class="hbtn">Supplement</div></a>&nbsp;<a href="https://github.com/rkyuca/medvt"><div class="hbtn">Code</div></a>
show_downloads: true
---



## Abstract 
<p style="text-align: justify">
Multiscale video transformers have been explored in a wide variety of vision tasks. To date, however, the multiscale processing has been confined to the encoder or decoder alone. We present a unified multiscale encoder-decoder transformer that is focused on dense prediction tasks in videos. Multiscale representation at both encoder and decoder yields key benefits of implicit extraction of spatiotemporal features (i.e. without reliance on input optical flow) as well as temporal consistency at encoding and coarse-to-fine detection for high-level (e.g. object) semantics to guide precise localization at decoding. Moreover, we propose a transductive learning scheme through many-to-many label propagation to provide temporally consistent predictions. We showcase our Multiscale Encoder-Decoder Video Transformer (MED-VT) on Automatic Video Object Segmentation (AVOS) and actor/action segmentation, where we outperform state-of-the-art approaches on multiple benchmarks using only raw images, without using optical flow.
</p>


## Method Overview

<img src="./data/medvt_fig_2.png" alt="Model" style="width:900">
<p style="text-align: justify">
Detailed (MED-VT) architecture with unified multiscale encoder-decoder transformer, illustrated with application to Automatic Video Object Segmentation (AVOS). The model has four functionally distinct components. (i) Backbone feature extractor to extract per frame features at multiple scales. (ii) Multiscale transformer encoder consisting of spatiotemporal within and between scale attention with resulting features; the multihead attention transformation is used for both. (iii) Multiscale transformer decoder consisting of pixel decoding, which produces decoded features and a series of mulitscale query learning decoder blocks, that iterate across scales, each of which entail self and cross attention, again using the multihead attention transformation. The input to the blocks are the decoded features and the query resulting from the previous block; the output is a final object query. The decoder applies an affinity between the learned query and the finest scale decoded features to yield an object attention map, which is concatenated with the finest scale decoded features for final decoder output (iv) A many-to-many label propagation and a shallow (three layer) 3D-CNN module that inputs decoder features to produce temporally consistent segmentation masks.</p>


## Qualitative Results

<table style="border-collapse: collapse; border: none;">
    <tr style="border: none;"> 
        <td style="border: none;text-align: center"> 
            <video width="380" height="300" controls>
                <source src="./data/davis-dance-twirl.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> <br> Davis (Dance-Twirl) 
        </td>
        <td style="border: none;text-align: center"> 
            <video width="380" height="300" controls>
                <source src="./data/breakdance_10.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>  <br> Davis(Breakdance)
        </td>
    </tr>
    <tr style="border: none;"> 
        <td style="border: none;text-align: center"> 
            <video width="380" height="300" controls>
                <source src="./data/moca-flounder_6.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> <br> MoCA(Flounder)-6  
        </td>
        <td style="border: none;text-align: center"> 
            <video width="380" height="300" controls>
                <source src="./data/hedgehog_1_10.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>  <br> MoCA(Hedgehog-1) 
        </td>
    </tr>
    <!--
    <tr style="border: none;"> 
        <td style="border: none;"> 
        <iframe width="320" height="240"
            src="https://youtu.be/JQw1WnCFodg">
        </iframe>
        <br> Davis  
        </td>
        <td style="border: none;"> 
        <iframe width="320" height="240"
        src="https://www.youtube.com/watch?v=yTKN0ZEsTIo">
        </iframe>
        <br> A2D 
        </td>
    </tr> -->
</table>


## Quantitative Results

| Backbone  | Davis'16 | YouTube-Objects | MoCA | A2D |
|---------- |----------|-----------------|------|-----|
| ResNet101 | 83.5 | 75.2 | 69.4 | 39.5 |
| SwinB     | 85.9 | 78.5 | 77.9 | 52.6 |


## Cite


```tex
@inproceedings{medvt23,
  title={ {MED-VT}: Multiscale Encoder-Decoder Video Transformer with Application to Object Segmentation},
  author={Rezaul Karim and He Zhao and Richard P. Wildes and Mennatullah Siam},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition },
  year={2023}
}
```







[Back To Home](../)
