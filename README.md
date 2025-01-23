# Text Normalization Project

## Overview
This project aims to normalize raw text data by identifying and extracting relevant tokens while filtering out redundant or irrelevant information. Two approaches were implemented for this task:

1. **BERT-Based Token Classification**: A fine-tuned BERT model was used to classify tokens as relevant or irrelevant.
2. **GPT-Based Few-Shot Prompting**: Azure OpenAI's GPT-4 model was leveraged using a few-shot prompting strategy.

---

## Approaches

### **BERT-Based Token Classification**
- The raw text (`raw_comp_writers_text`) was tokenized using BERT's tokenizer.
- Each token was labeled as `1` (relevant) or `0` (irrelevant) based on its presence in the normalized text (`CLEAN_TEXT`).
- The BERT model was fine-tuned for token classification and evaluated using precision, recall, and F1-score.

### **GPT-Based Few-Shot Prompting**
- A few-shot prompt with three examples was designed to guide GPT-4o in normalizing raw text.
- The model was queried via Azure OpenAI API to produce normalized text.

---

## Features
- Fine-tuning and evaluation of a BERT model for token classification.
- Integration with Azure OpenAI's GPT-4 for few-shot prompting.
- Token-level metrics (precision, recall, F1-score) for model evaluation.
- Support for both preprocessed test data and custom input testing.

---

## Installation

1. **Clone the Repository**:
   ``` bash
   git clone https://github.com/sotirisvl98/text-normalization.git
   ```
  
2. **Install Dependencies**: 
    ```bash
    pip install -r requirements.txt 
    ```
