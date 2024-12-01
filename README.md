# LLM-as-a-judge: Automated Evaluation of LLM Responses

This project implements an **LLM-as-a-judge** system to automate the evaluation of Large Language Model (LLM) responses. The approach leverages a language model to rate the quality of system-generated answers, simulating human judgment and providing a scalable and efficient solution for LLM evaluation. The system is designed to assess open-ended question-answer pairs based on various criteria, including relevance, clarity, and helpfulness.

## Features

- **Automated LLM Evaluation**: Uses an LLM to assess the quality of model-generated responses based on a defined set of criteria.
- **Improved Accuracy**: Refines the LLM's evaluation performance by adjusting the prompt structure, leading to a 30% increase in the correlation between LLM scores and human ratings.
- **Human Evaluation Dataset**: Leverages the `feedbackQA` dataset, which contains human ratings and feedback for a set of question-answer pairs, to establish a baseline for model performance.
- **Quantifiable Results**: Tracks performance improvements with measurable metrics like Pearson correlation to quantify the accuracy of LLM evaluation.

## Setup and Installation

To get started, clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/LLM-as-a-Judge.git
cd LLM-as-a-Judge
```

### Dependencies:
- `huggingface_hub`: Interface to Hugging Face's model hub for inference.
- `datasets`: Accesses and loads datasets, such as `feedbackQA`, for evaluation purposes.
- `pandas`: Data processing and manipulation.
- `tqdm`: Progress bar for loops and data processing.
- `re`: Regular expression for extracting scores from the LLM’s feedback.

## Results

- **Baseline Human Agreement**: Pearson correlation between two human raters was initially low (0.56) but was improved by filtering examples where raters agreed.
- **LLM Performance**: After refinement, the LLM-as-a-judge system demonstrated a **30% increase** in correlation with human scores.
- **Final Correlation**: The system achieved a **Pearson correlation of 0.86** between LLM and human ratings, showing reliable performance.

## Acknowledgments

- **Hugging Face** for providing access to powerful models and datasets.
- **McGill-NLP** for the `feedbackQA` dataset.
- Huggingface llm cookbook for code reference.
