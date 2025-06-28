# 🔍 Metaphor Detection using DistilBERT

This project explores metaphor detection using a fine-tuned DistilBERT model to classify metaphorical vs. literal usage of specific words in context. Built with a linguistically annotated dataset, the model determines whether a metaphor word (e.g., *road*, *candle*, *light*) is used figuratively or literally within a sentence.

---

## 🧠 Project Overview

Given a paragraph containing a target metaphor word, the system performs the following steps:

- Identifies the sentence containing the metaphor word.
- Determines whether the usage is **metaphorical** or **literal**.
- Fine-tunes **DistilBERT**, a lighter version of BERT, on a labeled dataset for **binary classification**.
- Leverages context-aware embeddings for accurate prediction.

---

## 🚀 Key Features

- ✅ Automatic extraction of sentences containing metaphor words  
- 🧠 Fine-tuning of DistilBERT for contextual metaphor detection  
- 🎯 Binary classification of metaphorical vs. literal usage  
- 🛑 Early stopping to prevent overfitting  
- 📊 Precision, Recall, and F1-Score evaluation  
- 💾 Saves model checkpoints and classification outputs  

---

## 🧾 Dataset Format

The dataset used in this project includes the following columns:

| Column        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `text`        | A paragraph or set of sentences containing a metaphor word                  |
| `metaphorID`  | An identifier mapped to a metaphor word (e.g., road, candle, light, etc.)   |
| `label_boolean` | Binary label (1 = Metaphorical, 0 = Literal)                             |

## 📚 Supported Metaphor Words

road, candle, light, spice, ride, train, boat

## 🛠️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/magantianirudh/Metaphor-Detection-using-NLP.git
cd Metaphor-Detection-using-NLP


2️⃣ Create Environment & Install Dependencies

```bash
pip install -r requirements.txt

3️⃣ Train the Model

```bash
python train.py --data_path path/to/your_dataset.csv

4️⃣ Evaluate & Save Results

```bash
python evaluate.py --model_path saved_model/ --test_data path/to/test.csv

## 📈 Evaluation Metrics
The performance of the model is measured using:

- Accuracy

- Precision

- Recall

- F1-Score

These metrics help in assessing how well the model distinguishes between literal and metaphorical usage in diverse contexts.

**Example:**
```csv
text,metaphorID,label_boolean
"The road to success is paved with failures.",road,1
"He walked along the dirt road for miles.",road,0
