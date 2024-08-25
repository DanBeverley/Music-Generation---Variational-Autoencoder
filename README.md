# Music Generation with Variational Autoencoder (VAE)

This project demonstrates the use of a Variational Autoencoder (VAE) for generating music. The model is trained on a dataset of music tracks and can generate new music samples by sampling from the learned latent space.


## Introduction

Variational Autoencoders (VAEs) are generative models that learn the underlying distribution of data in a latent space. This project utilizes a VAE to generate music by learning from the GTZAN dataset, which contains tracks from various music genres.

## Dataset

The project uses the GTZAN dataset for training. This dataset is publicly available and includes a variety of music genres. Ensure you have the dataset downloaded and accessible at the specified path in the code.

## Model Architecture

The VAE consists of an encoder and a decoder:

- **Encoder:** Maps the input music spectrograms to a latent space.
- **Latent Space:** A lower-dimensional representation where each point can generate a new music sample.
- **Decoder:** Reconstructs the music from the latent space back to the original spectrogram format.

## Training

The model is trained for a specified number of epochs on the GTZAN dataset. The training process involves minimizing the reconstruction loss and the KL-divergence to ensure the latent space follows a normal distribution.

### Hyperparameters:

- `train_size`: 60000
- `batch_size`: 10
- `epochs`: 10
- `latent_dim`: 2 (for visualization purposes)
- `test_size`: 10000

## Generating Music

After training, you can generate new music samples by sampling from the latent space. The notebook includes code to visualize and play the generated audio samples.

## Results

Results include the reconstructed music samples and latent space visualizations. The model's performance can be evaluated by listening to the generated music and comparing it with the original dataset.

## References

- Kingma, D. P., & Welling, M. (2014). Auto-Encoding Variational Bayes. arXiv preprint arXiv:1312.6114.
- The GTZAN Dataset: A large collection of music tracks categorized by genre, commonly used for training and evaluating models in music information retrieval.

---
