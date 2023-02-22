## Face Generation using GANs

This project explores the use of Generative Adversarial Networks (GANs) to generate new images of human faces that appear as realistic as possible. The project can be used for a variety of applications, such as generating new faces for computer games, designing avatars for social media platforms, or creating realistic training datasets for machine learning applications.

### Project Description

The generation of realistic human faces is a challenging task, but recent advancements in machine learning and deep neural networks have made it possible. This project uses a type of neural network called a GAN to generate new faces. The GAN consists of a generator network that generates new images and a discriminator network that learns to distinguish between real and fake images. Through a process of adversarial training, the generator learns to generate images that can fool the discriminator into thinking they are real.

### Dataset

The dataset used in this project is a preprocessed version of the CelebA dataset, which contains over 200,000 celebrity images. The images have been preprocessed to remove background noise, crop the faces, and align them to a common size. The preprocessed dataset contains 20,000 images and is available as a zip file [by clicking here](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/November/5be7eb6f_processed-celeba-small/processed-celeba-small.zip).

### Project Files

The project files are located in the project workspace and include the following files:

* `face_generation.ipynb`: Jupyter notebook with project developed
* `README.md`: this readme file
* `requirements.txt`: list of required Python libraries for this project
* `processed-celeba-small.zip`: dataset of celebrity faces preprocessed for the project

### Instructions

To get started, open the Jupyter notebook `face_generation.ipynb`. The project is organized into the following sections:

* **Data Pipeline**: Implementation of a data augmentation function and a custom dataset class to load the images and transform them.
* **Model Implementation**: Implementation of a custom generator and a custom discriminator to create the GAN.
* **Loss Functions and Gradient Penalty**: Implementation of loss functions and whether to use gradient penalty or not.
* **Training Loop**: Implementation of the training loop and the strategy to use.

### GAN Architecture

The GAN architecture used in this project consists of two main components: a generator network and a discriminator network. The generator network takes a random noise vector as input and generates a new image of a human face. The discriminator network takes an image as input and outputs a probability that the image is real or fake. During training, the generator tries to generate images that fool the discriminator, while the discriminator tries to correctly classify the real and fake images. The training process is iterative and continues until the generator is able to generate images that are indistinguishable from real images.

### Results

The model was able to generate primary facial features such as hair, eyes, nose, and mouth with some degree of success. However, the generated images appear abstract and artificial. This could be due to the limitations of the dataset used, which only consisted of images of white people. Furthermore, the low resolution of the input images after preprocessing also had an impact on the quality of the generated images.

### Conclusion

In conclusion, the GAN model was able to generate images of human faces, but the generated images lacked realism and variability. Future work could involve using higher resolution input images, modifying the generator and discriminator architecture, possibly using a pre-trained model like VGG, and experimenting with Wasserstain loss (WGAN) and gradient penalties to overcome issues with mode collapse and vanishing gradients. Additionally, the implementation of advanced GAN architectures such as StyleGAN or ProGAN could be explored to create more realistic, high-resolution images.








