# Paraphrase_Generation
# Model Training and Testing Instructions

## How to Run the Code

### 1. Clone the Repository
First, clone the repository:

```bash
git clone https://github.com/akkisai/Paraphrase_Generation.git
cd <your-repository-directory>
```

### 2. Testing and Training

Inside the `model_training` directory, there is a `testing.ipynb` notebook.  
You can open it to see examples of how to **load the model** and **start training**.

Alternatively, you can follow the steps below depending on which model you want to use:

---

### For **T5-Small**

Before running the below code, make sure to set your **root directory** properly.

```python
model_path = "./model_training/T5_small/checkpoint-30894"
token_path = "./model_training/T5_small/"

from transformers import T5ForConditionalGeneration, T5Tokenizer

model = T5ForConditionalGeneration.from_pretrained(model_path)
tokenizer = T5Tokenizer.from_pretrained(token_path)
```

---

### For **T5-Base**

Before running the below code, make sure to set your **root directory** properly.

```python
model_path = "./model_training/T5_base/"
token_path = "./model_training/T5_base/tokenizer"

from transformers import T5ForConditionalGeneration, T5Tokenizer

model = T5ForConditionalGeneration.from_pretrained(model_path)
tokenizer = T5Tokenizer.from_pretrained(token_path)
```

---

### For **T5-1000 (Limited Model)**

Before running the below code, make sure to set your **root directory** properly.

```python
limited_model_dir = "./t5_small_limited_final"

from transformers import T5ForConditionalGeneration, T5Tokenizer

model = T5ForConditionalGeneration.from_pretrained(limited_model_dir)
tokenizer = T5Tokenizer.from_pretrained(limited_model_dir)
```

---

## Notes
- Ensure that all the paths are correctly set according to your **local directory structure**.
- Install required libraries before running the notebooks:

```bash
pip install transformers torch
```

- Check the `testing.ipynb` notebook for complete examples of model loading, training, and evaluation.
