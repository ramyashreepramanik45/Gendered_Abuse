# Gendered Abuse Detection for Indic Languages

This repository contains code and instructions for detecting gendered abuse across Indic languages: Hindi, Tamil, and English. It supports three subtasks as defined in the shared task guidelines.

---

## 📂 Baseline_1 Overview

### 🔹 Subtask 1: Classification using Given Dataset

- Code is located in the `subtask_1/` folder.
- Dataset used: **ULI Dataset (label_1 only)**
- Files are available under `uli_dataset-main/training/` and `uli_dataset-main/testing/`.

#### 📊 Training Files:
- `train_en_l1.csv`
- `train_hi_l1.csv`
- `train_ta_l1.csv`

#### 📈 Testing Files:
- `test_en_l1.csv`
- `test_hi_l1.csv`
- `test_ta_l1.csv`

> ✏️ **Note:** Update file paths in the `.ipynb` notebooks to match the dataset structure before running.

---

### 🔹 Subtask 2: Transfer Learning with External Data

- Uses **external datasets** + **ULI dataset** for fine-tuning.

#### 🗃 External Datasets (Located in `Additional_Data/`):
- **MACD Dataset** (Hindi & Tamil):
  - `MACD_data/hindi_data/hindi_train.csv`
  - `MACD_data/hindi_data/hindi_val.csv`
  - `MACD_data/tamil_data/tamil_train.csv`
  - `MACD_data/tamil_data/tamil_val.csv`

- **HASOC Dataset** (English):
  - `HASOC_data/english_dataset.tsv`
  - `hasoc2019_en_test-2919.tsv`

#### 🔁 Fine-tuning Data (ULI Dataset):
- Use relevant files from `uli_dataset-main/training/` for final training.

> ✏️ Modify the paths inside the subtask_2 `.ipynb` notebooks before running.

---

### 🔹 Subtask 3: Multitask Learning

- Multi-label classification using `label_1` and `label_3` from the **ULI Dataset**.

#### 🧾 Files Used:
- **Training:**
  - `train_en_l1.csv`, `train_en_l3.csv`
  - `train_hi_l1.csv`, `train_hi_l3.csv`
  - `train_ta_l1.csv`, `train_ta_l3.csv`
  
- **Testing:**
  - `test_en_l1.csv`, `test_en_l3.csv`
  - `test_hi_l1.csv`, `test_hi_l3.csv`
  - `test_ta_l1.csv`, `test_ta_l3.csv`

> ✏️ Ensure to update paths in the `subtask_3/` notebooks to use correct files.

---

## 📁 Dataset Directory Structure

```
├── Additional_Data
│   ├── HASOC_data
│   │   ├── english_dataset.tsv
│   │   └── hasoc2019_en_test-2919.tsv
│   └── MACD_data
│       ├── hindi_data
│       │   ├── hindi_train.csv
│       │   └── hindi_val.csv
│       └── tamil_data
│           ├── tamil_train.csv
│           └── tamil_val.csv
├── structure.txt
└── uli_dataset-main
    ├── LICENSE
    ├── README.md
    ├── testing
    │   ├── test_en_l1.csv
    │   ├── test_en_l2.csv
    │   ├── test_en_l3.csv
    │   ├── test_hi_l1.csv
    │   ├── test_hi_l2.csv
    │   ├── test_hi_l3.csv
    │   ├── test_ta_l1.csv
    │   ├── test_ta_l2.csv
    │   └── test_ta_l3.csv
    └── training
        ├── train_en_l1.csv
        ├── train_en_l2.csv
        ├── train_en_l3.csv
        ├── train_hi_l1.csv
        ├── train_hi_l2.csv
        ├── train_hi_l3.csv
        ├── train_ta_l1.csv
        ├── train_ta_l2.csv
        └── train_ta_l3.csv


```