---
title: "STkM for Computer Vision"
excerpt: "We explore ensembling a CNN with our previously developed spatiotemporal clustering method, STkM, for the purpose of object detection in videos. <br/><img src='/images/stkm_pipeline.pdf'>"
collection: portfolio
---

So far, we have shown [STkM’s](http://OlgaD400.github.io/files/RTKM.pdf) superior ability to cluster moving objects of the simplest kind: points traveling in two dimensions. However, moving objects can be much more complex. Many objects that can be expressed as evolving, high-dimensional feature vectors, including videos. Therefore, we ensemble a pre-trained image CNN with STkM in an attempt to carry out region of interest detection in videos. 
We consider a video $F = [f_1, ... , f_T] \in \mathbb{R}^{T \times m \times N}$ to be a collection of $T$ frames, each containing $N$ pixels described by $m$ color channels. We also assume that we have a CNN, $R$ that maps images to some latent embedding space as follows, 
$$ R: \mathbb{R}^{m \times N} \to \mathbb{R}^{d \times p(N)} $$
where $d >> m$ and $p(\cdot)$ is a function that transforms our $N$ pixels into a grid of super-pixels that summarize local feature information, so that $p(N)$ is much less than $N$.
By applying the CNN to each frame of our video, we simultaneously enrich the feature space and diminish the number of points to be clustered. Our new input into STkM is $F' = [R(f_1), ..., R(f_T)]$. The proposed pipeline is visualized below on an example video.<br/><img src='/images/stkm_pipeline.pdf'>
