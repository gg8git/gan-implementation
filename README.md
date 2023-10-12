# GAN Implementation

This project is inspired by the following article: https://srome.github.io/An-Annotated-Proof-of-Generative-Adversarial-Networks-with-Implementation-Notes/

### Understanding the Proof of GANs

GANs are optimized by first optimizing the discriminator by k steps, then optimizing the generator to catch up to the capabilities of the discriminator. These steps are then alternated until the optimized generator is able to (in theory) create images that mimic the distribution of the sample images. At this point, the optimized discriminator should only be able to correctly identify the generated images 1/2 of the time. The discriminator and generator are optimized in tandem (in the aforementioned alternating fashion) in order to prevent the discriminator model from overfitting. 

These results can be obtained through creating an error function that balances the expected discriminator result for the sample image distribution and the generated image distribution, maximizing this function with respect to D, and minimizing this function with respect to G. Then, since D and G are simply multi-layer perceptron functions, this error function can be stochastically maximized or minimized. 

### Implementation Details
