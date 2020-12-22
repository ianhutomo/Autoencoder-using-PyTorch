# Autoencoder using PyTorch

Testing some implementation of AutoEncoder using PyTorch

- Denoising Auto Encoders
- Variational Auto Encoders

Define network with two groups of layers:
  * *Encoder Layers*: This part take an image and produce a low-dimensional "code" of the image. Therefore, the architecture of the network is narrowing down. Let's call this function <img src="https://render.githubusercontent.com/render/math?math=f^{\text{encoder}}">.
  * *Decoder Layers*: This part take a low-dimensional "code" of the image and produce the original image. Therefore, the architecture of the network is expanding. Let's call this function <img src="https://render.githubusercontent.com/render/math?math=f^{\text{decoder}}">.
  
Include some implementation to minimize the following loss:

<img src="https://render.githubusercontent.com/render/math?math=\mathcal{L} = \frac{1}{N} \sum_{i=1}^N \|x_i - f^{\text{decoder}}(f^{\text{encoder}}(x_i))\|_2^2">
