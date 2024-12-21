---

# Translation and Evaluation of NLLB Models

This repository contains Jupyter notebooks focused on translation tasks using NLLB (No Language Left Behind) models. The work encompasses model evaluation and fine-tuning techniques using LoRA (Low-Rank Adaptation) for Czech translations, providing insights into both performance metrics and practical applications.

---

## Overview

### Objectives
1. Evaluate the translation performance of NLLB models of varying sizes.
2. Fine-tune smaller NLLB models for low-resource languages like Czech using LoRA.
3. Analyze BLEU score improvements across model variations.

---

## Notebooks Included

### 1. Evaluation of Both NLLB Models
- **Title:** Larger Model
- **Key Features:**  
  - Evaluation of Czech translation performance.
  - Comparison of small and large NLLB models using BLEU scores:
    - **Small Model BLEU Score:** 3.61
    - **Large Model BLEU Score:** 19.90
  - Analysis of BLEU as the chosen metric for its:
    - Language-agnostic nature.
    - Ability to handle multiple valid answers.
    - n-gram matching to evaluate fluency and contextual accuracy.

### 2. Translation of Czech Using LoRA on NLLB Models
- **Title:** Smaller Model
- **Key Features:**  
  - Demonstrates LoRA fine-tuning on the smaller NLLB model.
  - Provides an efficient approach for adapting models to specific domains or low-resource language tasks.
  - Discusses trade-offs between computational cost and performance.

---

## Technical Details

### Models and Techniques
- **NLLB Models:**  
  NLLB is designed for low-resource language translation, offering pre-trained models of varying sizes to accommodate different computational resources and accuracy needs.
  
- **LoRA (Low-Rank Adaptation):**  
  LoRA introduces minimal trainable parameters to fine-tune large language models efficiently, making it an ideal method for adapting pre-trained models to specialized tasks.

### Metrics
- **BLEU Score:**  
  A widely used metric to evaluate the quality of machine-translated text by comparing it with a reference translation. Key benefits include:
  - Language independence.
  - Support for multiple valid translations.
  - Assessment of both fluency and contextual appropriateness.

---

## Results and Insights

### BLEU Score Analysis
- **Small Model vs. Large Model:**  
  The large NLLB model demonstrated a **5.5x improvement** in BLEU score over the smaller variant, emphasizing the trade-off between model size and translation accuracy.

### LoRA Fine-Tuning
- Showcased the potential of LoRA to make smaller models viable for low-resource translation tasks.
- Cost-effective solution for domain-specific translation requirements.

---

## Requirements

### Environment
- Python 3.8 or higher
- Jupyter Notebook

### Dependencies
Install all required libraries using:
```bash
pip install -r requirements.txt
```
**Key Libraries:**
- PyTorch
- Hugging Face Transformers
- LoRA integration tools (e.g., PEFT library)

---

## Usage Instructions

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd translation-nllb
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Run Jupyter Notebooks
Launch the notebooks using:
```bash
jupyter notebook
```

### Step 4: Execute Notebooks
Follow the structured steps in each notebook to:
1. Evaluate the BLEU score of NLLB models.
2. Fine-tune smaller models using LoRA.

---

## Key Learnings and Contributions

1. **Performance Trade-offs:**  
   Larger models yield higher BLEU scores but at a greater computational cost, while smaller models can be enhanced effectively with fine-tuning.

2. **LoRA Efficiency:**  
   LoRA enables cost-efficient domain adaptation, allowing smaller models to achieve near-large-model performance for specialized tasks.

3. **BLEU Metric Use:**  
   BLEU is a robust metric for translation tasks, offering insights into both accuracy and fluency.

4. **Applications in Low-Resource Settings:**  
   Fine-tuning strategies demonstrated here can be extended to other low-resource languages beyond Czech.

---

## Potential Extensions
- Experiment with additional fine-tuning methods like QLoRA (Quantized LoRA).
- Evaluate translation performance across different low-resource languages.
- Explore other evaluation metrics such as METEOR or TER for a comprehensive assessment.

---

