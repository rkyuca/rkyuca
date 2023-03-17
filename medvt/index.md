---
layout: default
title: <h2>MED-VT Multiscale Encoder Decoder Video Transformer.</h2>
description: <a href="https://rkyuca.github.io">Rezaul Karim</a>, <a href="https://joehezhao.github.io/">He Zhao</a>, <a href="https://lassonde.yorku.ca/users/wildes"> Richard P. Wildes</a>, <a href="https://msiam.github.io/homepage/">Mennatullah Siam</a><br><a href="">Paper</a>&nbsp;<a href="">Supplement</a>&nbsp;<a href="https://github.com/rkyuca/medvt">Code</a>
show_downloads: true
---



## Overview 
Multiscale video transformers have been explored in a wide variety of vision tasks. To date, however, the multiscale processing has been confined to the encoder or decoder alone. We present a unified multiscale encoder-decoder transformer that is focused on dense prediction tasks in videos. Multiscale representation at both encoder and decoder yields key benefits of implicit extraction of spatiotemporal features (i.e. without reliance on input optical flow) as well as temporal consistency at encoding and coarse-to-fine detection for high-level (e.g. object) semantics to guide precise localization at decoding. Moreover, we propose a transductive learning scheme through many-to-many label propagation to provide temporally consistent predictions. We showcase our Multiscale Encoder-Decoder Video Transformer (MED-VT) on Automatic Video Object Segmentation (AVOS) and actor/action segmentation, where we outperform state-of-the-art approaches on multiple benchmarks using only raw images, without using optical flow.


## Qualitative Results

<table style="border-collapse: collapse; border: none;">
    <tr style="border: none;"> 
        <td style="border: none;"> 
            <video width="320" height="240" controls>
                <source src="./data/davis-dance-twirl.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> <br> Davis (Dance-Twirl) 
        </td>
        <td style="border: none;"> 
            <video width="320" height="240" controls>
                <source src="./data/breakdance_10.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>  <br> Davis(Breakdance)
        </td>
    </tr>
    <tr style="border: none;"> 
        <td style="border: none;"> 
            <video width="320" height="240" controls>
                <source src="./data/moca-flounder_6.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> <br> MoCA  
        </td>
        <td style="border: none;"> 
            <video width="320" height="240" controls>
                <source src="./data/medvt_a2d.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>  <br> A2D 
        </td>
    </tr>
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
    </tr>
</table>


## Quantitative Results

| Backbone  | Davis'16 | YouTube-Objects | MoCA | A2D |
|---------- |----------|-----------------|------|-----|
| ResNet101 | 83.5 | 75.2 | 69.4 | 39.5 |
| SwinB     | 85.9 | 78.5 | 77.9 | 52.6 |


## Cite


```tex
@inproceedings{medvt,
  title={ {MED-VT}: Multiscale Encoder-Decoder Video Transformer with Application to Object Segmentation},
  author={Rezaul Karim and He Zhao and Richard P. Wildes and Mennatullah Siam},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition },
  year={2023}
}
```





[Back To Home](../)
