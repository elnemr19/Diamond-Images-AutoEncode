# Diamond-Images-AutoEncode

## 1. Project Description

This project aims to develop an **AutoEncoder** model to generate images accurately. Our approach involves training an  AutoEncoder model from scratch on the **Diamond Images dataset**.


![image](https://github.com/user-attachments/assets/b5396035-a8bd-4cdb-926c-120da30f30fe)


## 2. Table of Contents
[Dataset](https://github.com/elnemr19/Diamond-Images-AutoEncode/tree/main?tab=readme-ov-file#3-dataset)

[Pre-processing](https://github.com/elnemr19/Diamond-Images-AutoEncode/blob/main/README.md#4-pre-processing)

[Model Architecture](https://github.com/elnemr19/Diamond-Images-AutoEncode/blob/main/README.md#5--model-architecture)

[Results](https://github.com/elnemr19/Diamond-Images-AutoEncode/blob/main/README.md#6--results)


## 3. Dataset
-Source: Kaggle - [Diamond Images](https://www.kaggle.com/datasets/aayushpurswani/diamond-images-dataset/data)

-Description: The dataset contains eight classes, **{cushion, emerald, heart, marquise, oval, pear, princess, round}**

![image](https://github.com/user-attachments/assets/5d2d94f7-bc1a-4c12-a922-3519625ba60c)


## 4. Pre-processing

in this phase I:

* Resize my image to 64x64
* Do normalization on images by dividing each image by 255.0
* reshape images into 64 x 64 x 1
* Split my dataset into 80% for training, 20% for testing


## 5. 🧠 Model Architecture

This autoencoder model compresses grayscale diamond images into a latent representation and reconstructs them back to their original form. It consists of:

**1. Encoder**

Input: Grayscale images (img_size, img_size, 1).
Conv2D Layers: Extract spatial features with filters of sizes 32, 64, and 128, using ReLU activation.
MaxPooling: Reduces spatial dimensions progressively.

**2. Bottleneck**
Encodes essential image features into a compact representation.

**3. Decoder**

Conv2DTranspose Layers: Reconstruct features with filters of sizes 128, 64, and 32.
UpSampling: Restores the image to its original dimensions.
Output: Single Conv2DTranspose layer with sigmoid activation for pixel values in [0, 1].


## 6. 📊 Results

The autoencoder successfully reconstructed the grayscale diamond images, demonstrating its ability to compress and reconstruct visual information.

![image](https://github.com/user-attachments/assets/3fa4a97c-ab54-43df-9147-0119c6f3a5b1)


