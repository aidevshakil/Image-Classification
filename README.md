# Image Classification

![Project preview](test.png)

This is my image classification project built with Python, TensorFlow, and Streamlit. The app lets users upload an image and run predictions with either a pre-trained `MobileNetV2` model or a custom-trained `CIFAR-10` classifier.

## Overview

The project is designed to demonstrate practical image classification through a simple web interface. It includes:

- `MobileNetV2 (ImageNet)` for general-purpose object recognition
- A custom `CIFAR-10` model for classifying 10 common categories
- A `Streamlit` interface for easy model selection and image upload
- Real-time prediction output with confidence scores

## Models Used

### MobileNetV2

This model uses TensorFlow's pre-trained `ImageNet` weights and can recognize a wide range of everyday objects.

### CIFAR-10 Model

This model is trained to classify images into the following categories:

- airplane
- automobile
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

## Project Structure

```text
Image-Classification/
├── app.py              # Streamlit app
├── train.py            # Script to train the CIFAR-10 model
├── cifar10_model.h5    # Saved trained model
├── requirements.txt    # Project dependencies
├── test.png            # README preview image
└── Some Testing Images/ # Sample images for testing
```

## Getting Started

### Prerequisites

- Python 3.7 or later
- `pip`

### Installation

```bash
git clone <your-repository-url>
cd Image-Classification
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

On Windows, activate the environment with:

```bash
venv\Scripts\activate
```

## Run the App

```bash
streamlit run app.py
```

After starting the server, open `http://localhost:8501` in your browser if it does not open automatically.

## How to Use

1. Launch the Streamlit app.
2. Choose a model from the sidebar.
3. Upload a `.jpg` or `.png` image.
4. View the predicted class and confidence score.

## Training

If you want to retrain the CIFAR-10 model, run:

```bash
python train.py
```

This will train the model and save a new `cifar10_model.h5` file in the project folder.

## Tech Stack

- Python
- Streamlit
- TensorFlow / Keras
- NumPy
- Pillow

## Notes

- `MobileNetV2` downloads pretrained weights from TensorFlow when needed.
- The CIFAR-10 model expects images resized to `32x32`.
- MobileNetV2 input images are resized to `224x224`.

## Author

This project is maintained by Shakil.
