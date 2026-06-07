# Squishy Robotics - Wildfire Multimodal Forecasting

This repository contains my research artifacts for a **wildfire multimodal forecasting** project conducted through the **Berkeley Expert Systems Technologies (BEST) Lab** in collaboration with **Squishy Robotics**. The project explores how RGB imagery, near-infrared imagery, segmentation masks, and textual descriptors can support interpretable wildfire-spread and fire-intensity modeling for robotic situational awareness.

Official background for the research setting is available through the [BEST Lab](https://best.berkeley.edu/) and the [Corsican Fire Database](https://pro.universita.corsica/article.php?id_art=2133&id_rub=572), the external wildfire image dataset used in this project. BEST Lab also documents Squishy Robotics' emergency-response and wildfire-monitoring context in its [Squishy Robotics coverage](https://best.berkeley.edu/2024/07/02/squishy-robotics-on-the-cover-of-soft-robotics/).

## Contents

- **Datasets**: Corsican Fire Database images, ground-truth masks, helper utilities, and controlled-burn reference materials used during exploration.
- **Repo**: Exploratory notebooks and model-development notebooks for RGB/NIR data processing, descriptor generation, and multimodal fire forecasting.
- **Logistics**: Meeting, planning, and project-management artifacts from the research collaboration. Administrative access forms and signed agreements are intentionally excluded.

## Research Scope

- Conducted exploratory analysis of the **Corsican Fire Database**, including RGB images, near-infrared images, manually extracted fire-region masks, and metadata describing fire and scene conditions.
- Built prototype pipelines for image preprocessing, descriptor generation, model training, and late-fusion forecasting.
- Investigated whether visual streams and text descriptors can jointly support interpretable predictions of fire area, intensity, superposition, and spread direction.

## Methods and Tools

- **Data preparation**: Image cleaning, RGB/NIR pairing, mask-based feature extraction, metadata normalization, and exploratory data analysis.
- **Computer vision**: PyTorch, torchvision, EfficientNet, image transforms, and mask-derived fire metrics.
- **Language and descriptors**: BERT-style descriptor embeddings and Gemini-assisted descriptor generation experiments.
- **Temporal modeling**: LSTM and late-fusion model prototypes combining visual and text-derived features.
- **Evaluation**: Accuracy reports, tolerance-based numeric evaluation, exploratory plots, and notebook-level qualitative review.

## Key Outputs

- Exploratory analysis notebooks for the Corsican wildfire imagery and metadata.
- Prototype multimodal forecasting notebooks combining RGB, near-infrared, and descriptor features.
- Research notes and presentation materials supporting a wildfire-response robotics research workflow.

## How to Navigate

- Start with `Repo/Corsican EDA.ipynb` for dataset exploration and descriptive analysis.
- Use `Repo/fire_pred.ipynb` for the initial multimodal forecasting workflow.
- Use `Repo/fire_pred_LateFusion.ipynb` for late-fusion modeling experiments.
- Use `Datasets/Corsican Data Set/` for the local working copy of images, masks, helper functions, and dataset metadata.

## Reproducibility Notes

This repository preserves a research prototype rather than a polished software package. Some notebooks were developed in Google Colab and may contain historical output cells, local drive paths, or collaborator-specific execution metadata.

To rerun Gemini-assisted cells, create a local environment variable instead of placing keys in notebooks:

```powershell
$env:GOOGLE_API_KEY = "your-key"
```

Install the approximate Python dependencies with:

```powershell
pip install -r requirements.txt
```

The Corsican Fire Database is an external dataset maintained by Universita di Corsica. Follow the dataset provider's access and license terms before redistributing or reusing the data.

## Academic Integrity Note

This repository contains my own research code, exploratory notebooks, and project artifacts, shared for portfolio and research transparency. Do not copy this work for active or future coursework, and follow your institution's academic integrity policies.
