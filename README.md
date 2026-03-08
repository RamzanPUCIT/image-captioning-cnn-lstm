# Image Captioning using CNN + LSTM

This project implements an **Image Captioning System** using deep learning that automatically generates textual descriptions for images.

The model uses a **CNN Encoder (ResNet50)** to extract image features and an **LSTM Decoder** to generate captions word-by-word.

---

## Project Overview

Image captioning is a task that combines **Computer Vision and Natural Language Processing**.

Given an image, the model generates a meaningful natural language description.

Example:

Image → "A man riding a bike on the street."

---

## Architecture

Encoder–Decoder Architecture:

Image → **ResNet50 CNN Encoder** → Feature Vector → **LSTM Decoder** → Caption


CNN (ResNet50)
↓
Image Features (2048)
↓
Embedding + LSTM
↓
Word Prediction


---

## Dataset

Dataset used:

**Flickr30k Image Captioning Dataset**

https://www.kaggle.com/datasets/hsankesara/flickr-image-dataset

Dataset contains:

- 31,000 images
- 5 captions per image

---

## Methodology

Pipeline:

1. Image preprocessing
2. Caption cleaning and tokenization
3. Feature extraction using ResNet50
4. Caption sequence generation
5. Training an Encoder–Decoder model
6. Caption generation for test images

---

## Model Architecture

Encoder:
- ResNet50 (pretrained on ImageNet)
- Output feature size: 2048

Decoder:
- Embedding Layer
- LSTM (256 units)
- Dense layer with Softmax

---

## Training

Training setup:

- Loss Function: Categorical Crossentropy
- Optimizer: Adam
- Epochs: 10
- Early Stopping used
- Model Checkpoints saved

Best validation loss:


val_loss ≈ 3.83


---

## Results

The model successfully learned sentence structure and generated captions for unseen images.

Example Generated Caption:


a man in a black shirt is sitting on a bench with a man in a blue shirt


While captions are grammatically correct, some predictions remain generic.

---

## Technologies Used

- Python
- TensorFlow / Keras
- ResNet50
- LSTM
- Google Colab

---

## Repository Structure


image-captioning-resnet50-lstm
│
├── image_captioning_flickr30k.ipynb
├── README.md
├── requirements.txt


---

## Future Improvements

Possible improvements include:

- Attention Mechanism
- Transformer-based captioning models
- Beam Search decoding
- BLEU score evaluation

---

## Author

Muhammad Ramzan  
M.Phil Artificial Intelligence  
PUCIT – University of the Punjab Lahore
