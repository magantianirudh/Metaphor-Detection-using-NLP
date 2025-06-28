# 🔍 Metaphor Detection with DistilBERT

This project leverages a fine-tuned **DistilBERT** model to classify whether specific words (e.g., *road*, *candle*, *light*) are used metaphorically or literally in a given context. Built on a linguistically annotated dataset, it offers a lightweight yet powerful approach to metaphor detection using NLP.

---

## 📖 Overview

The system processes a paragraph, identifies the sentence with a target metaphor word, and predicts its usage as **metaphorical** (e.g., "The road to success") or **literal** (e.g., "The dirt road"). By fine-tuning DistilBERT, the model captures contextual nuances for accurate binary classification.

---

## ✨ Features

- 🛠️ Extracts sentences containing metaphor words automatically
- ⚙️ Fine-tunes DistilBERT for metaphor vs. literal classification
- 📏 Uses early stopping to prevent overfitting
- 📊 Evaluates with **Accuracy**, **Precision**, **Recall**, and **F1-Score**
- 💾 Saves model checkpoints and predictions
- 🎯 Supports metaphor words: *road*, *candle*, *light*, *spice*, *ride*, *train*, *boat*

---

## 📊 Dataset Structure

The dataset consists of:

| Column          | Description                                              |
|-----------------|----------------------------------------------------------|
| `text`          | Paragraph or sentences with a metaphor word              |
| `metaphorID`    | Identifier for the metaphor word (e.g., *road*, *candle*) |
| `label_boolean` | Binary label (1 = Metaphorical, 0 = Literal)            |

**Example:**
```csv
text,metaphorID,label_boolean
"The road to success is paved with failures.",road,1
"He walked along the dirt road for miles.",road,0
```

---

## 🛠️ Setup & Usage

### 1. Clone the Repository
```bash
git clone https://github.com/magantianirudh/Metaphor-Detection-using-NLP.git
cd Metaphor-Detection-using-NLP
```

### 2. Set Up Environment
```bash
pip install -r requirements.txt
```

### 3. Train the Model
```bash
python train.py --data_path path/to/your_dataset.csv
```

### 4. Evaluate & Save Results
```bash
python evaluate.py --model_path saved_model/ --test_data path/to/test.csv
```

---

## 📈 Performance Metrics

The model is evaluated using:
- **Accuracy**: Overall correctness of predictions
- **Precision**: Proportion of correct metaphorical predictions
- **Recall**: Ability to identify all metaphorical instances
- **F1-Score**: Harmonic mean of precision and recall

These metrics ensure robust performance across varied contexts.

---

## 🚀 Next Steps
- Explore additional metaphor words
- Enhance dataset with more diverse examples
- Experiment with other transformer models (e.g., BERT, RoBERTa)
