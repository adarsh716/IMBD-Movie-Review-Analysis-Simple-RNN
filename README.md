# IMDB Movie Review Sentiment Analysis using Simple RNN

An end-to-end deep learning project for binary sentiment classification (Positive/Negative) on the IMDB movie reviews dataset using a Simple Recurrent Neural Network (RNN) and an interactive Streamlit web application.

🔗 **Live Demo**: [IMDB Sentiment Analyzer on Streamlit Community Cloud](https://imbd-movie-review-analysis-simple-rnn-wpahu5lyhdepkhfwptcyex.streamlit.app/)

---

## 📌 Features

- **Deep Learning Model**: Built with TensorFlow/Keras using an Embedding layer, Simple RNN layer, and Dense sigmoid output.
- **Interactive Web App**: Powered by Streamlit to classify custom movie reviews in real time.
- **Educational Notebooks**: Covers word embeddings, end-to-end model training with early stopping, and step-by-step prediction pipelines.

---

## 📁 Repository Structure

```text
simpleRNN/
├── embedding.ipynb       # Introduction to word embeddings & one-hot encoding
├── simplernn.ipynb       # Model training, evaluation, and saving
├── prediction.ipynb      # Standalone inference & prediction testing
├── simple_rnn_imdb.h5    # Pre-trained Simple RNN model weights
├── main.py               # Streamlit web application
├── requirements.txt      # Python dependencies
├── LICENSE               # MIT License
└── README.md             # Project documentation
```

---

## 🧠 Model Architecture

The model is trained on the Keras IMDB dataset:
- **Vocabulary Size (`max_features`)**: 10,000 words
- **Sequence Length (`maxlen`)**: 500 tokens (padded/truncated)
- **Architecture**:
  - `Embedding(input_dim=10000, output_dim=128, input_length=500)`
  - `SimpleRNN(units=128, activation='relu')`
  - `Dense(units=1, activation='sigmoid')`
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Callbacks**: Early Stopping (`monitor='val_loss'`, `patience=5`)

---

## 🚀 Getting Started

### 1. Prerequisites
- Python 3.9 - 3.11 recommended

### 2. Installation

Clone or download this repository, then navigate to the project directory:

```bash
cd simpleRNN
```

Create and activate a virtual environment:

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 💻 Usage

### 🌐 Live Demo
Access the live deployed application directly in your browser:
👉 **[Open Streamlit App](https://imbd-movie-review-analysis-simple-rnn-8cmvzfhycd3ya324effhuz.streamlit.app)**

### Run Locally
Launch the Streamlit app locally:

```bash
streamlit run main.py
```

Open your browser at the URL shown in your terminal (usually `http://localhost:8501`), enter a movie review, and click **Classify** to see whether it is classified as **Positive** or **Negative** along with the prediction score.

### Explore the Notebooks

Launch Jupyter Notebook or Jupyter Lab:

```bash
jupyter notebook
```

- [`embedding.ipynb`](file:///c:/Aiengineer/simpleRNN/embedding.ipynb): Learn word embeddings and text preprocessing.
- [`simplernn.ipynb`](file:///c:/Aiengineer/simpleRNN/simplernn.ipynb): Train the RNN model on the IMDB dataset from scratch.
- [`prediction.ipynb`](file:///c:/Aiengineer/simpleRNN/prediction.ipynb): Test sample predictions on custom reviews.

---

## 📜 License

This project is open source and available under the [MIT License](file:///c:/Aiengineer/simpleRNN/LICENSE).
