

# Automated Classification of BBC Articles

## Project Overview

This project implements a deep learning model to classify BBC news articles into different categories. Using a dataset of BBC news articles, I've developed a text classification model that can accurately categorize articles into predefined classes such as business, entertainment, politics, sport, and tech.

## Dataset

I used the [BBC News Classification dataset](https://www.kaggle.com/competitions/learn-ai-bbc/data) from Kaggle. The dataset consists of:

- A training set with 1,490 articles, each containing an ArticleId, Text, and Category.
- A test set with 735 articles, containing only ArticleId and Text.

The average length of articles (after stopword removal) is approximately 223 words.

## Model Architecture

I implemented a sequential model using TensorFlow and Keras with the following layers:

1. Embedding layer
2. Bidirectional LSTM layer
3. Another Bidirectional LSTM layer
4. Dense layer with softmax activation

## Performance

My model achieved impressive results:

- Training Accuracy: 99.76%
- Validation Accuracy: 96.64%
- Validation Loss: 0.1374

![Accuracy_and_Loss_over Epochs](https://github.com/user-attachments/assets/9914f2aa-810a-4e61-96ba-667309153cab)

The plot above shows the training and validation accuracy and loss over epochs, demonstrating the model's learning progress and performance.

## Key Features

1. **Data Preprocessing**: 
   - Removal of stopwords
   - Lemmatization of words
   - Tokenization and padding of sequences

2. **Model Training**:
   - Use of early stopping and model checkpointing for optimal performance
   - Training/Validation split of 80/20

3. **Hyperparameters**:
   - Vocabulary size: 1,000
   - Maximum sequence length: 120
   - Embedding dimension: 16

## Code Structure

The main components of the project are:

- Data loading and preprocessing
- Model definition and training
- Evaluation and visualization
- Prediction on test set

## How to Use

1. Download the Python Notebook
2. Run all cells

## Results

The model successfully classifies news articles into five categories. Here's a sample of the predictions:

```
ArticleId    Category
1018         sport
1319         entertainment
1138         sport
459          entertainment
1020         business
```

## Future Improvements

- Experiment with different model architectures
- Implement cross-validation for more robust evaluation
- Fine-tune hyperparameters for potentially better performance

## Contributing

Feel free to fork this project and submit pull requests with any improvements or suggestions!

## License

This project is open-source and available under the MIT License.
