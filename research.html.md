---
title: "Research"
echo: false
section-divs: false
keep-md: true
---


## Post-Training Augmentation Invariance
This work develops a framework for post-training augmentation invariance, in which our goal is to add invariance properties to a pretrained network without altering its behavior on the original, non-augmented input distribution. We define this notion precisely and additionally introduce augmented encoders, which are probabilistic encoders that formalize augmentation-based encoding processes and that serve as our fundamental object of study. We introduce two losses for augmented encoders, namely, Markov-Wasserstein minimization and Wasserstein correlation maximization, and we demonstrate empirically that both losses can be used to train lightweight, one-hidden-layer MLP adapter networks $E_{\theta}$ that, when appended to the latent space of a pretrained network $F$, do indeed lead to (approximate) post-training augmentation invariance. For example, on STL10 with $F=\textrm{DINOv2}$ features, the composite network $C\circ E_{\theta}\circ F$, where $C$ is a linear classifier and where $E_{\theta}$ is one of our proposed adapter networks, achieves $94\%$ classification accuracy on arbitrarily rotated images, whereas a network of the form $C\circ F$ without the adapter $E_{\theta}$ drops to $71\%$ accuracy. Similarly, we can boost noise-invariant classification results from $58\%$ up to $86\%$. Significantly, we obtain these results with no fine-tuning (the weights of $F$ remain frozen throughout), and our methods introduce little corruption to the original features, since $E_{\theta}$ acts nearly isometrically on the non-augmented latent distribution. In contrast, we show that adapter networks trained with alternative candidate losses, specifically SimCLR and HSIC maximization, produce uncompetitive classification results and fundamentally corrupt the original latent space.

(Paper currently under review.)

[PDF](assets/PostTrainingAugmentationInvariance_Preprint_v1.pdf){target="_blank"} | [Code](https://github.com/keenan-eikenberry/augmentation_invariance)


## Bayesian Inference for Markov Kernels Valued in Wasserstein Spaces 
This is my doctoral work re-packaged in standard formatting. I analyze quantitative and structural aspects of Bayesian inference using Markov kernels, Wasserstein metrics, and Kantorovich monads. In particular, I show the the following main results: first, that Markov kernels can be viewed as Borel measurable maps with values in a Wasserstein space; second, that the Disintegration Theorem can be interpreted as a literal equality of integrals using an original theory of integration for Markov kernels; third, that the Kantorovich monad can be defined for Wasserstein metrics of any order; and finally, that, under certain assumptions, a generalized Bayes’s Law for Markov kernels provably leads to convergence of the expected posterior distribution in the Wasserstein metric to an optimal value. These contributions provide a basis for studying further convergence, approximation, and stability
properties of Bayesian inverse maps and inference processes using a unified theoretical framework that bridges between statistical inference, machine learning, and probabilistic programming semantics. 

[PDF](assets/MarkovKernelsValuedInWassersteinSpaces.pdf){target="_blank"}