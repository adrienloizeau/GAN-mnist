# GAN-mnist
This notebook uses two Generative Adversarial Network models to generate fake samples of the MNIST dataset.

- The first model is a simple one with only linear modules for both the generative and the discriminative model.
- The second one takes the architecture of the DCGAN model from Google.


The generator network follows this architecture:
- **Input**: A random noise vector is fed into the generator as input.
- **Transposed convolutional layers:** A series of transposed convolutional layers are used to gradually increase the spatial resolution of the image while decreasing the number of channels. These layers are interleaved with batch normalization and ReLU activation.
- **Output:** The final layer in the generator uses a tanh activation function, to produce images with pixel values between -1 and 1.

The discriminator network follows this architecture:
- **Input:** An image is fed into the discriminator as input.
- **Convolutional layers**: A series of convolutional layers are used to extract features from the input image. These layers are interleaved with LeakyReLU activation.
- **Fully connected layers:** Fully connected layers are used to classify the input image as real or fake. The final layer in the discriminator uses a sigmoid activation function to produce a probability of the image being real.

Note: Here we will only use 4 Convolution layers not 5.

<img src="images/DCGAN architecture.png" alt="Alt text" title="DCGAN architecture">


This exercise was created for the Msc AI class at Centralesupélec.
