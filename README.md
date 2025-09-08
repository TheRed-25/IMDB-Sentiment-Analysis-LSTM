# IMDB Sentiment Analysis with LSTM 🚀

![IMDB Sentiment
Banner](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat&logo=tensorflow)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)

![License](https://img.shields.io/badge/License-MIT-green?style=flat)🔍
**A deep learning project for binary sentiment classification on IMDB
movie reviews.**\
This Jupyter Notebook builds an LSTM-based neural network to analyze
sentiments (positive/negative) from the IMDB dataset. It includes data
preprocessing, model training, evaluation with ROC curves, and custom
review predictions.📈

## 🌟 Features

-   **Dataset Handling**: Loads and preprocesses the IMDB dataset (25K
    training + 25K test reviews). 📚
-   **Model Architecture**: Embedding + LSTM + Dense layers with dropout
    for robust performance. 🧠
-   **Training & Evaluation**: Trains for 5 epochs, evaluates accuracy
    (\~84%), and plots ROC curves (AUC \~0.93). 📊
-   **Custom Predictions**: Test the model on your own movie reviews!
    ✅/❌
-   **Visualizations**: Accuracy plots and ROC curves using Matplotlib.
    🎨

## 🛠️ Installation

1.  Clone the repo:

    ``` bash
    git clone https://github.com/shervinnd/IMDB-Sentiment-Analysis-LSTM.git
    cd IMDB-Sentiment-Analysis-LSTM
    ```

2.  Install dependencies (use a virtual environment recommended):

    ``` bash
    pip install tensorflow numpy matplotlib scikit-learn
    ```

3.  Open the Jupyter Notebook:

    ``` bash
    jupyter notebook IMBD.ipynb
    ```

## 🚀 Usage

1.  **Run the Notebook**: Execute cells sequentially to load data,
    build/train the model, and evaluate.

2.  **Custom Review Testing**: Use the `encode_text` function for new
    reviews. Example:

    ``` python
    sample_text = "This movie was amazing!"
    encoded = encode_text(sample_text)
    prediction = model.predict(encoded)
    print("Positive ✅" if prediction[0][0] > 0.5 else "Negative ❌")
    ```

3.  **Visualize Results**: Check the ROC curve plot for performance
    insights. 📉

## 🧩 Model Architecture

``` plaintext
- Embedding Layer: 10,000 vocab size, 32 dimensions, input length 200.
- LSTM Layer: 64 units.
- Dense Layer: 64 units (ReLU) + Dropout (0.5).
- Output: Sigmoid for binary classification.
```

Compiled with Adam optimizer and binary cross-entropy loss. Achieves
\~84% test accuracy after 5 epochs! 💪

## 📊 Results

-   **Test Accuracy**: 84.26% ✅
-   **ROC AUC**: \~0.93 (visualized in the notebook).\
    Example Predictions:
-   "The movie was fantastic and I really enjoyed it" → Positive ✅
-   "The movie was terrible and I absolutely hated it" → Negative ❌

Training History (sample):

  Epoch   Train Acc   Val Acc
  ------- ----------- ---------
  1       55.78%      82.80%
  5       95.31%      84.38%

## 🤝 Contributing

Pull requests welcome! For major changes, open an issue first. 😊

1.  Fork the repo.
2.  Create a feature branch (`git checkout -b feature`).
3.  Commit changes (`git commit -m`).
4.  Push to the branch (`git push origin feature`).
5.  Open a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file
for details.
