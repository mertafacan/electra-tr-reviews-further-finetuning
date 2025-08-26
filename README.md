# Domain Specific Fine-Tuning for Turkish Product Reviews

[![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)](https://python.org)
[![uv](https://img.shields.io/badge/uv-package%20manager-purple.svg)](https://github.com/astral-sh/uv)
[![Transformers](https://img.shields.io/badge/🤗-Transformers-yellow.svg)](https://huggingface.co/transformers/)

> **Domain-Adaptive Fine-tuning**: Comparison of a published ELECTRA checkpoint (baseline) with domain-specific fine-tuning for Turkish product reviews.

This project investigates the impact of **further fine-tuning (domain-adaptive training)** on Turkish product reviews by using an already fine-tuned ELECTRA model as the baseline.

## 📁 Project Structure

| File | Description |
|------|-------------|
| `electra-tr-reviews-further-finetuning.ipynb` | 📓 Main notebook: baseline evaluation → domain-adaptive fine-tuning → comparison |
| `turkish_product_reviews_train.csv` | 📊 Domain-specific training dataset ([Turkish product reviews](https://huggingface.co/datasets/fthbrmnby/turkish_product_reviews)) |
| `out-fine-tuned-model/` | 💾 Domain-adaptive fine-tuning outputs and checkpoints |
| `pyproject.toml` | ⚙️ Project configuration |
| `uv.lock` | 🔒 Dependency lock file |

## 🚀 Quick Start

This project uses the [uv](https://github.com/astral-sh/uv) package manager.  
All dependencies are defined in the `uv.lock` file.

### Prerequisites

- Python 3.12 or higher
- [uv](https://github.com/astral-sh/uv) package manager

### Installation
#### Using uv (recommended)

1. **Clone the repository**:

   ```powershell
   git clone https://github.com/mertafacan/Electra-Tr-Product-Reviews-DAFT.git
   cd Electra-Tr-Product-Reviews-DAFT
   ```

2. **Install uv**:

   ```powershell
   # if not installed
   pip install uv
   ```

3. **Create environment**:

   ```powershell
   uv venv
   .venv\Scripts\activate
   ```
   

4. **Install project dependencies**:

   ```powershell
   uv sync
   ```

### Usage

Run the notebook with uv:

```powershell
# open directly in VS Code
code electra-tr-reviews-further-finetuning.ipynb
```
or
```powershell
# Jupyter notebook (alternative) 
uv run jupyter notebook
```

## 🤖 Model Comparison

### Baseline Model

* **Pre-trained**: [`incidelen/electra-small-turkish-sentiment-analysis-cased`](https://huggingface.co/incidelen/electra-small-turkish-sentiment-analysis-cased)
* Already fine-tuned for general Turkish sentiment analysis

### Domain-Adaptive Fine-tuning

* **Dataset**: [Turkish product reviews](https://huggingface.co/datasets/fthbrmnby/turkish_product_reviews) (domain-specific)
* **Approach**: Further fine-tuning on the published checkpoint
* **Output**: Domain-adapted checkpoints saved in `out-fine-tuned-model/`

### Evaluation & Comparison

* **Baseline Performance**: Performance of the published model on product reviews
* **Further Fine-tuning Performance**: Performance after domain-adaptive training
* **Metrics**: Accuracy, F1-score, classification report, and confusion matrix
* **Analysis**: Examination of domain adaptation impact and performance 

## 📬 Contact

Mert Afacan – [https://www.linkedin.com/in/mert-afacan/](https://www.linkedin.com/in/mert-afacan/) – [mert0afacan@gmail.com](mailto:mert0afacan@gmail.com)
