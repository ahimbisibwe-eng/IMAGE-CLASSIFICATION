# African Health AI — TEAM HEALTH

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahimbisibwe-eng/IMAGE-CLASSIFICATION/blob/main/C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb)

> **Building responsible medical AI with African data, foundation models and human expertise.**

**African Health AI** is an African-led health AI initiative by **TEAM HEALTH**, emerging from the **ACT Africa 2026 Foundation Models Workshop**. The current prototype explores how medical foundation models can be adapted and evaluated using African health data to support future, human-centred medical imaging solutions.

**Team Leader:** **Bernard Ahimbisibwe**  
**Country:** Uganda  
**Current prototype:** MedSigLIP Foundation Model for Chest X-Ray Classification

---

## Innovation Café Positioning

African Health AI is being developed in response to the need for **locally relevant, responsible and evidence-based AI capabilities for African health systems**.

The current prototype uses Google's **MedSigLIP-448** medical foundation model with a **Nigeria Chest X-Ray Dataset** to explore zero-shot classification of four categories:

- NORMAL
- COVID-19
- TB
- PNEUMONIA

The prototype demonstrates that an existing medical foundation model can be practically evaluated with African data in a relatively accessible computing environment. At the same time, the results highlight important requirements for responsible deployment, including better African datasets, local validation, model adaptation, clinical oversight, infrastructure, skills and appropriate governance.

The long-term direction is to move from a single-dataset research prototype toward a broader **African Health AI** platform and research ecosystem.

---

## The African Development Challenge

African health systems face challenges related to access to specialised diagnostic expertise, medical imaging capacity, representative datasets, AI skills and locally validated digital health technologies.

At the same time, many advanced AI models are developed using datasets that may not adequately represent African populations, health facilities, disease patterns and imaging environments.

This creates an important gap:

**Advanced AI capability exists, but African evidence, data, validation capacity and responsible deployment pathways need to be strengthened.**

African Health AI addresses this gap by exploring foundation models using African data and by treating model limitations and validation requirements as part of the innovation process.

---

## The Current Solution

### MedSigLIP Chest X-Ray Prototype

The current working prototype uses:

- **Model:** `google/medsiglip-448`
- **Dataset:** Nigeria Chest X-Ray Dataset
- **Task:** Zero-shot chest X-ray classification
- **Classes:** NORMAL, COVID-19, TB, PNEUMONIA
- **Framework:** PyTorch + Hugging Face Transformers
- **Environment:** Google Colab
- **GPU:** NVIDIA T4 in the reported experiment

The prototype includes:

1. Dataset loading and quality checks
2. Zero-shot medical image classification
3. Accuracy and macro F1 evaluation
4. Image embedding generation
5. PCA dimensionality reduction
6. t-SNE visualisation
7. Grad-CAM/visual interpretability analysis
8. Analysis of classification errors and model limitations

---

## Prototype Evidence

The current notebook reports:

| Metric | Result |
|---|---:|
| Accuracy | **55.33%** |
| Macro F1 | **0.5435** |
| Embedding size | **600 × 1152** |
| PCA retained variance — 50 dimensions | **90.25%** |

The reported experiment used **500 training images and 150 test images per class** across four classes.

These results are presented as **research evidence of technical feasibility**, not as evidence of clinical effectiveness. The current performance also demonstrates why African-context validation and model adaptation are necessary before any clinical deployment.

---

## From Prototype to African Health AI

The development pathway is:

**African health data**  
↓  
**Foundation models**  
↓  
**Local adaptation and fine-tuning**  
↓  
**African-context evaluation**  
↓  
**Human-in-the-loop validation**  
↓  
**Responsible health-system integration**

The longer-term objective is to investigate whether this approach can be extended across multiple African datasets, institutions and health contexts.

The project does **not** assume that performance on one African dataset automatically generalises to other African populations or health systems.

---

## Innovation-to-Policy Relevance

African Health AI provides a practical case for discussing the ecosystem conditions required for responsible medical AI in Africa.

Key questions include:

### Data
How can African countries develop representative, high-quality and responsibly governed medical datasets?

### Skills
How can African researchers, developers and health professionals build the capacity to develop, evaluate and use foundation models?

### Infrastructure
What computing, connectivity, data and health-information infrastructure is required for sustainable AI development?

### Validation
How should medical AI systems be evaluated across different African populations, hospitals, imaging equipment and clinical environments?

### Governance
What ethical, regulatory, privacy and accountability mechanisms should guide medical AI?

### Human oversight
How can AI support health workers while maintaining appropriate clinical responsibility?

### Financing and sustainability
How can African health AI move from research prototypes and workshops toward sustainable pilots and locally owned solutions?

---

## Potential Development Impact

### Near term

- Demonstrate an African health AI prototype.
- Build practical foundation-model skills among African innovators and researchers.
- Generate evidence about the opportunities and limitations of medical foundation models.
- Encourage the use of African datasets in AI research.

### Medium term

- Expand evaluation to additional African datasets.
- Fine-tune/adapt models for African health contexts.
- Establish stronger medical-AI evaluation benchmarks.
- Develop partnerships with universities, researchers, hospitals and health institutions.

### Long term

- Contribute to validated AI decision-support research.
- Strengthen African capacity to develop and evaluate medical AI.
- Support responsible adoption of AI in health systems.
- Contribute evidence to African AI governance and digital-health policy.

---

## Why African Data Matters

The current prototype uses Nigerian chest X-ray data as an initial African dataset. It is **not presented as representative of the entire African continent**.

Future work should investigate data from multiple African settings to understand how differences in:

- population characteristics;
- disease prevalence;
- imaging equipment;
- healthcare environments;
- clinical practices; and
- data quality

affect model performance.

This is central to the project's approach: **African AI should be tested with African evidence rather than assuming that models developed elsewhere will automatically generalise.**

---

## Main Notebook

**Notebook:** [`C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb`](./C_of_ACT_2026_Foundation_MedSigLIP_Workshop_.ipynb)

The notebook contains the complete working Google Colab workflow used for the experiment, including environment setup, dataset preparation, MedSigLIP inference, evaluation, embeddings, dimensionality reduction and visual analysis.

> **Important:** The original working Colab notebook is preserved unchanged. The README and supporting repository files have been developed around the notebook without modifying its working model code.

---

## Reproducing the Prototype

1. Click the **Open in Colab** badge at the top of this README.
2. Enable a GPU runtime if available.
3. Run the notebook's setup cells.
4. Obtain the authorised Nigeria chest X-ray dataset referenced by the notebook.
5. Run the notebook cells in sequence.

Results may vary according to model revisions, package versions, dataset versions, hardware and random seeds.

---

## Environment

The reported environment included:

- Python 3.12.13
- PyTorch 2.11.0+cu128
- Transformers 5.16.1
- KaggleHub 1.0.2
- Hugging Face Hub 1.28.0
- NVIDIA T4 GPU

See [`requirements.txt`](./requirements.txt) for the main package versions recorded for reproducibility.

---

## Repository Structure

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

The supporting folders are documentation placeholders and are intentionally separated from the original notebook.

---

## Team

### TEAM HEALTH

**Team Leader:** Bernard Ahimbisibwe  
**Country:** Uganda

TEAM HEALTH developed the prototype during the **ACT Africa 2026 Foundation Models Workshop**, exploring practical applications of foundation models to African community challenges.

The team's interests include:

- Medical AI
- Foundation models
- African datasets
- Responsible AI
- AI governance
- Health technology
- Research and innovation capacity

---

## Workshop Context

This project was developed during the **ACT Africa 2026 Foundation Models Workshop**, where participants explored foundation models, African datasets and practical AI applications.

The workshop provided the initial technical foundation for the current prototype. African Health AI is the proposed longer-term direction for extending that work beyond a single workshop experiment.

---

## Responsible AI and Clinical Safety

This project is a **research and educational prototype**.

It is **not a clinical diagnostic system** and should not be used to make medical decisions.

Before any real-world clinical use, substantial additional work would be required, including appropriate dataset governance, ethical review, clinical validation, external validation, safety evaluation, regulatory assessment and human oversight.

The project treats these requirements as central to responsible African health AI development.

---

## Research Direction

Future research may investigate:

- Fine-tuning MedSigLIP using African medical datasets
- Multi-country African health datasets
- African-context medical AI benchmarks
- Explainability and clinical interpretability
- External and prospective validation
- Robustness across hospitals and imaging equipment
- Human-in-the-loop clinical workflows
- Privacy-preserving health AI
- Responsible AI governance
- Sustainable deployment models

---

## Citation

If you use this repository or build on the prototype, please acknowledge:

**TEAM HEALTH — African Health AI**  
**Team Leader: Bernard Ahimbisibwe, Uganda**

Please also acknowledge the underlying model and dataset sources according to their respective terms and citation requirements.

---

## Disclaimer

This repository is provided for research and educational purposes. The reported results do not establish clinical effectiveness, diagnostic accuracy in clinical practice, or suitability for deployment. Any future clinical application would require appropriate validation, governance, regulatory review and qualified clinical oversight.
