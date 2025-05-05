# IMDb Sentiment Classification with Teacher–Student Distillation
This project implements a **teacher–student network** for sentiment classification
- Fine-tune a **teacher model** (BERT).
- Train a **smaller student model** (DistilBERT) using **knowledge distillation**.

The student model learns from both the **ground truth labels** and the **soft predictions (logits)** of the teacher.
## Folder Structure

│
├── Main.ipynb        
│
├── Loop
    ├── loopOFproject.mov          

## Steps to Run the App
### 1. Clone the Repository
```bash
git clone https://github.com/isha-harish/IMDb_Sentiment_Classification-Teacher-StudentDistillation.git
cd IMDb_Sentiment_Classification-Teacher-StudentDistillation
```
### 2.Run 
Open Main.ipynb in Jupyter or Google Colab.
Run all cells from top to bottom.

## 📝 Performance Discussion
The student model retains about 99% of the teacher’s accuracy while being smaller and faster. The slight drop (∼0.6% in accuracy/F1) is expected, but AUC remains high (~97%), indicating strong discriminative performance.
This shows that knowledge distillation is effective for compressing large models into smaller ones with minimal performance loss—making the student model a good choice for deployment when resources are limited.

## 📊 Results

| Model                   | Accuracy | F1 Score | AUC    |
|-------------------------|----------|----------|--------|
| **Teacher (BERT)**      | 0.9162   | 0.9180   | 0.9745 |
| **Student (DistilBERT)**| 0.9102   | 0.9078   | 0.9721 |



