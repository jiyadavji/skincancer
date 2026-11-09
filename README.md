# Skin Cancer Detection Using Deep Machine Learning Techniques

A full-stack AI healthcare application for skin lesion classification and segmentation, with explainable predictions and fairness across skin tones. Won 2nd Prize at a college-level technical exhibition.

> **Disclaimer:** This is a clinical decision-support tool, not a replacement for a dermatologist.

## Features

- Image upload and prediction dashboard
- Lesion classification and segmentation visualization
- Results history
- AI diagnostic assistant
- Secure role-based access for clinicians and admins
- Health risk and hospital resource forecasting using XGBoost

## Highlights

### Accuracy
97.4% accuracy on lesion classification.

### Multi-task CNN
Performs classification, segmentation, growth trend prediction, and uncertainty estimation together.

### Ensemble Learning
VGG16, ResNet50, and EfficientNet-B0 combined through an XGBoost meta-learner, with temperature-scaled softmax for calibrated confidence.

### Explainability
SHAP heatmaps and LIME explanations, cross-checked against the dermatological ABCD rule.

### Fairness
Melanin modulation layer, evaluated across Fitzpatrick skin types I-VI, targeting under 2% accuracy variation between skin tones.

### Multispectral Feature Engineering
Melanin and hemoglobin maps reconstructed from RGB using physics-based reflectance models (Beer-Lambert law).

### Advanced Augmentation
GAN-based synthetic images, diffusion-based lesion progression simulation, metadata-aware augmentation, and skin tone balancing.

## Dataset

HAM10000: 10,015 dermoscopic images across 7 lesion classes, with age, gender, and lesion site metadata.

## Tech Stack

| Layer | Technology |
|---|---|
| Deep Learning | TensorFlow 2.15, Python 3.10 |
| Frontend | React.js |
| Database | PostgreSQL |
| Forecasting | XGBoost |
| Explainability | SHAP, LIME |
| Training Hardware | NVIDIA RTX 4090 |

## Training Details

- Input size: 256x256
- Optimizer: Adam (learning rate 1e-4)
- Epochs: 36

## Installation

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
cd frontend
npm install
```

## Usage

```bash
# Backend
python app.py

# Frontend
cd frontend
npm start
```

Open `http://localhost:3000` in your browser.

## Scope

**Included:** classification, segmentation, explainability, fairness evaluation, forecasting, demo application.

**Not included:** real-time clinical deployment, EHR integration, live patient data collection.
