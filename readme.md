```markdown
# Skin Disease Detection – Phase 1 (HAM10000)

This project implements a **skin disease classification model** using the **HAM10000** dataset.  
It covers Phase-1 of the Major Project:  
✔ Dataset loading  
✔ Preprocessing  
✔ Splitting  
✔ Training EfficientNetB0  
✔ Metrics & Visualizations  
✔ Single-image prediction  

---

## 📂 Project Structure

```

Major/
│── notebook/
│── outputs/                 # Small PNG images only (plots)
│── .gitignore
│── Major.ipynb              # Main training + prediction notebook
│── requirements.txt         # Python dependencies

```

⚠️ **Dataset and large models are NOT included** (kept out intentionally for size & licensing).  
You must download HAM10000 manually.

---

## 📥 1. Download HAM10000 Dataset

Download from Kaggle:  
https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000

Place the files like this:

```

Major/
└── data/
└── raw/
├── HAM10000_metadata.csv
├── HAM10000_images_part_1/
│      ├── ISIC_*.jpg
├── HAM10000_images_part_2/
├── ISIC_*.jpg

````

---

## 🛠️ 2. Install Requirements

### Option A — with Conda (recommended)
```bash
conda create -n skinproj python=3.10 -y
conda activate skinproj
pip install -r requirements.txt
````

### Option B — with venv

```bash
python -m venv venv
venv\\Scripts\\activate   # Windows
pip install -r requirements.txt
```

---

## ▶️ 3. Run Jupyter Notebook

```bash
jupyter notebook
```

Open:

**`Major.ipynb`**

Run all cells from top to bottom.

You will get:

* Class distribution
* Sample image grid
* Train/validate split
* EfficientNetB0 model
* Accuracy & loss curves
* Confusion matrix
* Single-image prediction

---

## 📷 4. To Run Single Image Prediction

Inside the notebook, find the **Single-image inference cell** and set:

```python
img_path = "../data/raw/HAM10000_images_part_1/ISIC_XXXXXXX.jpg"
```

The notebook loads the model (via saved weights + builder) and prints:

* Top-3 predicted classes
* Probabilities
* Input image preview

---

## ✔️ 5. Important Notes

* The dataset is **not included** due to GitHub file size limits.
* The notebook automatically ignores dataset paths and large model files due to the `.gitignore`.
* All teammates must download the dataset individually into `data/raw/`.
* Training will run again on any machine following this README.

---

## 👥 6. Adding Collaborators

On GitHub:
`Settings → Collaborators → Add GitHub username`

Teammates can then:

```bash
git clone https://github.com/aryan-099/Skin-Disease-Detection-Major.git
```

---

## ⚠️ Disclaimer

This project is for **academic and research purposes** only.
It is **NOT** a medical diagnostic tool.

---
