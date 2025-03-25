# Gendered Abuse Detection for Indic Languages

This repository contains code and instructions for detecting gendered abuse across Indic languages: Hindi, Tamil, and English. It supports three subtasks as defined in the shared task guidelines.

---

## Baseline_1 Overview

### 🔹 Subtask 1: Classification using Given Dataset
- Code files are available in the `subtask_1/` folder.
- Data is available in the `dataset/` folder.
- Dataset used: **ULI Dataset**
- Only `label_1` is used for this task.

####  Training Data
- Tamil: `train_ta_l1.csv`
- English: `train_en_l1.csv`
- Hindi: `train_hi_l1.csv`

####  Testing Data
- Tamil: `test_ta_l1.csv`
- English: `test_en_l1.csv`
- Hindi: `test_hi_l1.csv`

>  **Note:** Make sure to change the file paths in the respective `.ipynb` files before running.

---

### 🔹 Subtask 2: Transfer Learning with External Data

- External datasets are used along with the ULI dataset for training.
  
#### 🗃 External Datasets:
- **MACD (Hindi & Tamil):** [MACD GitHub Repo](https://github.com/ShareChatAI/MACD/tree/main/dataset_80_10_10)
- **HASOC (English):** [HASOC 2019 Dataset](https://hasocfire.github.io/hasoc/2019/dataset.html)

- Finetuning is done using the given **ULI dataset**.
- All required data is available inside the `dataset/` folder.

> **Note:** Change the file paths in the `.ipynb` notebooks accordingly before running.

---

### 🔹 Subtask 3: Multitask Learning

- Uses the given **ULI dataset**.
- Task setup involves multi-task classification on:
  - `label_1` – Gendered abuse
  - `label_3` – Explicit/Aggressive content

#### 🗃 Files Used:
- Training and testing data for `label_1` and `label_3` from ULI dataset

>  **Note:** Modify file paths in the respective `.ipynb` files and run.

---

## 📁 Folder Structure

