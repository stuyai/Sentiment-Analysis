# Sentiment Analysis Project

This project focuses on sentiment analysis using a Convolutional Neural Network (CNN) model built with TensorFlow and Keras. The model is trained to classify the sentiment of hotel reviews as either positive or negative. 

This project was built by Will Nzeuton, with help from Otzar Jaffe and Elias Xu.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Prediction](#prediction)
- [License](#license)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/stuyai/sentiment_analysis.git
    cd sentiment_analysis
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. Download the dataset:
    ```sh
    !wget https://stuyai.org/download/reviews.csv
    ```

2. Run the Jupyter notebook:
    ```sh
    jupyter notebook STUYAI_SENTIMENTAL_ANALYSIS_FULL.ipynb
    ```

## Project Structure

```
sentiment_analysis/
├── data/
│   └── reviews.csv
├── models/
│   └── sentiment_model.h5
├── notebooks/
│   ├── STUYAI_SENTIMENTAL_ANALYSIS_FULL.ipynb
│   └── STUYAI_SENTIMENTAL_ANALYSIS_BLANK.ipynb
├── README.md
├── LISCENSE and other files
└── requirements.txt
```

## Model Architecture

The model consists of the following layers:
- Embedding layer
- Convolutional layers with MaxPooling
- Dense layers with Dropout
- Output layer with softmax activation

## Training

The model is trained using the following hyperparameters:
- `max_features`: 12000
- `embedding_dim`: 32
- `sequence_length`: 600
- `epochs`: 4
- `batch_size`: 16
- `validation_split`: 0.1

## Evaluation

The model is evaluated on a test set, and the accuracy is printed:
```sh
Test Accuracy: 0.9563
```

## Prediction

To make predictions on new reviews, use the `predict` function defined in the notebook:
```python
new_reviews = ["The hotel was fantastic!", "I had a terrible experience."]
predict(new_reviews)
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.