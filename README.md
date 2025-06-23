# Palm Vein Verification using Siamese Networks

This project implements an end-to-end biometric verification system using **palm vein images** and a **Siamese Neural Network**, built entirely in a **single Jupyter Notebook**. It demonstrates how deep learning can be applied to intrinsic biometrics with limited data, using **few-shot learning**.

---

## Key Highlights

- Based on the **CASIA-MS-PalmprintV1** dataset
-  **Siamese architecture** for one-shot or few-shot learning
-  **ROI extraction** using classical image processing techniques
-  **Gabor filtering** to enhance vein patterns
-  Uses **contrastive loss** for similarity learning
-  Entire workflow — from preprocessing to model training — is implemented in a single notebook

---

## Dataset Used

- **Name**: [CASIA-MS-PalmprintV1](http://www.cbsr.ia.ac.cn/MS_PalmprintDatabase.asp)
- **Captured At**: Six different wavelengths
- **We Used**: Images captured at **850nm**, shown to be most effective for palm vein visibility

> Dataset must be requested directly from CASIA for academic purposes.

---

##  Architecture Summary

### Siamese Network
- Two identical CNN branches extract 128D embeddings from palm images
- L1 distance between embeddings is used to compute similarity
- Output is a probability score using sigmoid activation

### Preprocessing Pipeline
- Wrist removal (fixed cropping)
- Otsu thresholding
- Largest connected component extraction
- ROI cropping using maximum inscribed square
- Gabor filter application for texture enhancement

All steps are executed sequentially in the notebook.

---

## How to Run

1. **Clone the repository** and navigate into the project directory:
   ```bash
   git clone https://github.com/your-username/palm-vein-verification.git
   cd palm-vein-verification
   ```

2. **Install dependencies** (recommended inside a virtual environment):
    ```bash
    pip install -r requirements.txt
    ```

3.  **Download the dataset** from the provided link under the Datasets used section.


4.  **Launch the notebook** and run all cells sequentially:
    - Performs ROI extraction using classical image processing

    - Applies Gabor filtering to enhance palm vein features

    - Trains the Siamese network using contrastive loss

    - Displays training metrics (accuracy, loss, etc.)

---

## Report
The report on this project work can be found under [docs folder](./doc/).


