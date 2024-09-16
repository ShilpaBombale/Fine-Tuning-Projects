# Fine-Tune Small Language Models for Sentiment Analysis of IMDb Dataset

This project demonstrates the fine-tuning of two pre-trained small language models, **DistilBERT** and **ALBERT**, for sentiment analysis using the IMDb dataset. The task involves classifying movie reviews as either 'positive' or 'negative'. Additionally, the project leverages **Low-Rank Adaptation (LoRA)** to make the fine-tuning process more resource-efficient.

## Files in This Repository

### 1. `distilbert.ipynb`
- Jupyter notebook containing the fine-tuning process for the **DistilBERT** model.
- Includes steps for loading the IMDb dataset, preparing the model for sequence classification, and fine-tuning.
- Outputs performance metrics such as **accuracy, precision, recall**, and an **ROC curve**.

### 2. `albert.ipynb`
- Jupyter notebook for fine-tuning the **ALBERT** model.
- Similar structure to `distilbert.ipynb`, covering data loading, model setup, and LoRA-enhanced fine-tuning.
- Includes performance evaluation and comparison with DistilBERT in terms of sentiment classification accuracy.

### 3. `Final_Report.pdf`
- Detailed project report explaining the methodologies, performance evaluations, and findings.
- Provides a comparison of the fine-tuning processes and results between DistilBERT and ALBERT.
- Includes visualizations such as **ROC curves** and comparison charts.

## Models Used

### 1. **DistilBERT** (`distilbert-base-uncased`)
- A smaller and faster variant of BERT with approximately **70 million parameters**.
- Well-suited for tasks requiring fewer resources without sacrificing much performance.

### 2. **ALBERT** (`albert-base-v2`)
- A lightweight BERT model variant with only **11.8 million parameters**.
- Designed to reduce memory consumption and improve training speed while maintaining high performance.

### Dataset
- **IMDb Sentiment Dataset** with **2,000 movie reviews**, evenly split into training and validation sets.

## Methodology

### Fine-Tuning Process
- Both models are fine-tuned for sentiment analysis using the **Hugging Face** library, adapting them to classify IMDb movie reviews.

### Low-Rank Adaptation (LoRA)
- **LoRA** is used to reduce the number of trainable parameters, optimizing fine-tuning for lower resource consumption.

### Performance Metrics
- **Accuracy, Precision, Recall, F1-score**, and **ROC Curves** are used to evaluate model performance.

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/repositoryname.git

   ## How to Use

2. Open the Jupyter notebooks (`distilbert.ipynb` or `albert.ipynb`) in your Jupyter environment (e.g., JupyterLab, Google Colab).

3. Follow the instructions within the notebooks to:
   - Load the IMDb dataset
   - Fine-tune the models
   - Evaluate their performance

## Results

- **DistilBERT** and **ALBERT** both perform effectively on the sentiment classification task.
- **ALBERT**, with fewer parameters, offers a more resource-efficient alternative while maintaining competitive performance.
- **LoRA** significantly reduces the computational overhead for fine-tuning.

## Conclusion

This project demonstrates the practical application of fine-tuning small language models, specifically **DistilBERT** and **ALBERT**, for sentiment analysis using the **Hugging Face** ecosystem. The use of **LoRA** ensures efficient resource usage without sacrificing model performance, making these techniques highly applicable in resource-constrained environments.

