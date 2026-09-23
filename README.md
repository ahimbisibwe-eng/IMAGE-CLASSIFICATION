# MedSigLIP Foundation Model for Chest X-Ray Classification

A Google Colab research notebook developed during the **ACT Africa 2026 Foundation Models Workshop** for exploring medical image classification with Google's **MedSigLIP** model and an African chest X-ray dataset.

> **Important:** The original working Colab notebook is preserved unchanged. This repository adds documentation and reproducibility files around the notebook; the model code itself has not been modified.

## Project overview

This project explores zero-shot medical image classification using `google/medsiglip-448` on a Nigeria chest X-ray dataset. The experiment considers four diagnostic categories:

- NORMAL
- COVID-19
- TB
- PNEUMONIA

The work is motivated by the need to explore AI approaches that can support medical imaging research in African settings, where access to specialised diagnostic expertise and representative datasets can be limited.

## Main notebook

**Notebook:** [`C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb`](./C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb)

The notebook contains the complete Google Colab workflow used for the experiment, including environment setup, dataset preparation, MedSigLIP inference, evaluation, embeddings, dimensionality reduction and visual analysis.

## Reported experimental results

The current notebook reports the following zero-shot classification results:

| Metric | Result |
|---|---:|
| Accuracy | **55.33%** |
| Macro F1 | **0.5435** |
| Embedding size | **600 × 1152** |
| PCA retained variance (50 dimensions) | **90.25%** |

The experiment used four classes with 500 training images and 150 test images per class in the reported setup.

## Model

- **Model:** `google/medsiglip-448`
- **Framework:** PyTorch + Hugging Face Transformers
- **Execution environment:** Google Colab
- **GPU used:** NVIDIA T4 in the reported Colab environment

## Dataset

The notebook uses the **Nigeria Chest X-Ray Dataset** accessed through KaggleHub. The dataset contains chest X-ray images organised into the four classification categories used in the experiment.

The repository does **not** include the dataset files. Users should obtain the dataset through its authorised source and follow the applicable dataset licence and usage conditions.

## Key analysis

The notebook includes analysis of:

1. Dataset loading and quality checks
2. Zero-shot MedSigLIP classification
3. Accuracy and macro F1 evaluation
4. Confusion between diagnostic classes
5. Image embeddings
6. PCA dimensionality reduction
7. t-SNE visualisation
8. Grad-CAM/visual interpretability analysis

A notable observation in the reported evaluation was confusion between **COVID-19** and **PNEUMONIA**, illustrating the difficulty of distinguishing visually similar chest X-ray patterns in zero-shot classification.

## Environment

The reported environment included:

- Python 3.12.13
- PyTorch 2.11.0+cu128
- Transformers 5.16.1
- KaggleHub 1.0.2
- Hugging Face Hub 1.28.0
- NVIDIA T4 GPU

See [`requirements.txt`](./requirements.txt) for the main package versions recorded for reproducibility.

## Reproducing the experiment

1. Open the main `.ipynb` file in Google Colab.
2. Enable a GPU runtime if available. The original experiment was run using an NVIDIA T4.
3. Use the notebook's setup cells to install dependencies.
4. Obtain the authorised Nigeria chest X-ray dataset referenced by the notebook.
5. Run the notebook cells in sequence.

Results can vary depending on package versions, model revisions, dataset versions, hardware and random seeds.

## Repository structure

```text
IMAGE-CLASSIFICATION/
│
├── C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── README.md
│
├── results/
│   └── README.md
│
└── src/
    └── README.md
```

The folders are documentation placeholders. They are intentionally kept separate from the original notebook so that the working Colab code remains untouched.

## Research direction

This repository is an experimental foundation for further work on medical AI using African datasets. Future work may investigate:

- Fine-tuning MedSigLIP on locally relevant datasets
- Better class balancing and dataset quality control
- African-context medical image benchmarks
- Explainability and clinical interpretability
- External validation on additional datasets
- Robust evaluation across hospitals, regions and acquisition settings
- Responsible deployment and human-in-the-loop clinical workflows

The reported results are research results, **not a clinical diagnostic system**. They should not be used to make medical decisions without appropriate clinical validation and oversight.

## Workshop context

This work was developed in the context of the **ACT Africa 2026 Foundation Models Workshop**, with an interest in building practical AI capabilities around African data and community challenges.

## Author

**Bernard Ahimbisibwe**  
Uganda

Research interests include artificial intelligence, foundation models, medical AI, African datasets, digital learning and responsible AI for development.

## Citation

If you use this repository or build on the notebook, please acknowledge the repository and the underlying dataset/model sources.

## Disclaimer

This project is for research and educational purposes. The model outputs should not be interpreted as medical diagnoses or as evidence of clinical effectiveness.
