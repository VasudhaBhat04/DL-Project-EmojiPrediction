# 😊 Emoji Prediction from Text using Bi-LSTM & GloVe

This project explores the use of deep learning to predict appropriate emojis for social media posts (like tweets), making text-based communication more expressive. Inspired by how platforms like Twitter suggest emojis based on typed text, we’ve trained a model to automatically predict the most relevant emoji given a phrase.

This project focuses on building an intelligent emoji prediction system using deep learning,specifically a Bi directional Long Short Term Memory (Bi-LSTM) model. 
Bi-LSTM networks are excellent at processing sequences and understanding context from both directions which makes them perfect for analyzing natural language.
For this project, we worked with a lightweight version of the SemEval 2018 Emoji Prediction dataset, which originally involved a much larger and more complex collection of tweets. Given our limited computational resources, we opted for a simplified, preprocessed version that still captured the essence of the task without the overhead of millions of noisy tweet samples.

The dataset we used contained around 5,000 English text samples, each paired with one of 20 frequently used emojis, and was carefully curated to be balanced, with 250 samples per emoji. This made it manageable to train on, while still being representative enough for meaningful emoji prediction.

 ## Model Architecture

- **Embedding Layer**: Pre-trained GloVe (100D)
- **Bidirectional LSTM Layer (64 units)**: Learns from text in both forward and backward directions.
- **Dropout Layer**: Prevents overfitting.
- **Dense Layers**: Used for classification.
- **Output Layer**: 20 neurons (softmax activation)

### Loss and Optimizer
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam

## Performance

- **Training Accuracy**: ~73%
- **Validation Accuracy**: ~88%
- **Test Accuracy**: ~87% (evaluated on separate test split)
  
 The project successfully delivered a working emoji predictor powered by deep learning.
 Using Bi-LSTM and GloVe word embeddings, the system was able to learn how different words and phrases relate to specific emojis.The model performed well, and evaluation tools like confusion matrices and training validation plots helped confirm that it was learning the right patterns. With an added feature to suggest the top 3 emojis, the tool becomes even more user friendly
