# Gendered Abuse Detection for Indic Languages

This repository contains code and instructions for detecting gendered abuse across Indic languages: Hindi, Tamil, and English. It supports three subtasks as defined in the shared task guidelines.

---

## Instructions to run Code

### 🔹 Subtask 1: Classification using Given Dataset

- Code is located in the `final_codes/TASK1/fusion_hurtlex/` folder.
- Dataset used: **ULI Dataset (label_1 only) and Hurtlex data files**
- Embedding Used: **Glove** for english and **fastext** for tamil,hindi
- Files are available under `uli_dataset-main/training/`,`uli_dataset-main/testing/` and `dataset/Additional_Data/Hurtlex`.

#### Training Files:
- `train_en_l1.csv`
- `train_hi_l1.csv`
- `train_ta_l1.csv`

#### Testing Files:
- `test_en_l1.csv`
- `test_hi_l1.csv`
- `test_ta_l1.csv`

> **Note:** Update file paths in the `.ipynb` notebooks to match the dataset structure before running.

---

### 🔹 Subtask 2: Transfer Learning with External Data

- Uses **external datasets** + **HurtLex** + **ULI dataset** for fine-tuning.
- Code is located in the `final_codes/TASK2` folder.
####  External Datasets (Located in `Additional_Data/`):

- **MACD Dataset** (Hindi & Tamil):  
  [MACD GitHub Repo – dataset_80_10_10](https://github.com/ShareChatAI/MACD/tree/main/dataset_80_10_10)

- **HASOC Dataset** (English):  
  [HASOC 2019 Dataset](https://hasocfire.github.io/hasoc/2019/dataset.html)


- Embedding Used: **Glove** for english and **fastext** for tamil,hindi

##### Local File Structure:
- `MACD_data/hindi_data/hindi_train.csv`
- `MACD_data/hindi_data/hindi_val.csv`
- `MACD_data/tamil_data/tamil_train.csv`
- `MACD_data/tamil_data/tamil_val.csv`
- `HASOC_data/english_dataset.tsv`
- `HASOC_data/hasoc2019_en_test-2919.tsv`
- `dataset/Additional_Data/Hurtlex/hurtlex_EN.tsv`
- `dataset/Additional_Data/Hurtlex/hurtlex_HI.tsv`

####  Fine-tuning Data (ULI Dataset):
- Use relevant files from `uli_dataset-main/training/` for final training.

>  Modify the paths inside the subtask_2 `.ipynb` notebooks before running.

---

### 🔹 Subtask 3: Multitask Learning

- Multi-label classification using `label_1` and `label_3` from the **ULI Dataset** and **HurtLex Files**
- Embedding Used: **Glove** for english and **fastext** for tamil,hindi
- Code is located in the `final_codes/TASK3` folder.
#### Files Used:
- **Training:**
  - `train_en_l1.csv`, `train_en_l3.csv`
  - `train_hi_l1.csv`, `train_hi_l3.csv`
  - `train_ta_l1.csv`, `train_ta_l3.csv`
  
- **Testing:**
  - `test_en_l1.csv`, `test_en_l3.csv`
  - `test_hi_l1.csv`, `test_hi_l3.csv`
  - `test_ta_l1.csv`, `test_ta_l3.csv`

>  Ensure to update paths in the `subtask_3/` notebooks to use correct files.

---
### 🔹 Abuse Lexicon

- **HurtLex** (English):  
  [Hurtlex English](https://github.com/valeriobasile/hurtlex/tree/master/lexica/EN/1.0)

- **HurtLex** (Hindi):  
  [Hurtlex Hindi](https://github.com/valeriobasile/hurtlex/tree/master/lexica/HI/1.0)



##  Directory Structure

```
├── baseline_1
│   ├── subtask1
│   │   ├── 1_combined.ipynb
│   │   ├── 1_english.ipynb
│   │   ├── 1_hindi.ipynb
│   │   └── 1_tamil.ipynb
│   ├── subtask2
│   │   ├── combined_2.ipynb
│   │   ├── eng_2.ipynb
│   │   ├── hindi_2.ipynb
│   │   └── tamil_2.ipynb
│   └── subtask3
│       ├── Combined_subtask3.ipynb
│       ├── English_subtask3.ipynb
│       ├── Hindi_subtask3.ipynb
│       └── Tamil_subtask3.ipynb
├── Baseline2
│   ├── TASK1
│   │   ├── task1-english-base2.ipynb
│   │   ├── task1-hindi-cnn-bilstm.ipynb
│   │   └── task1-tamil-cnn-bilstm.ipynb
│   ├── TASK2
│   │   ├── task2-eng-cnn-bilstm.ipynb
│   │   ├── task2-hindi-cnn-bilstm.ipynb
│   │   └── task2-tamil-cnn-bilstm.ipynb
│   └── TASK3
│       ├── task3_eng_lstm_cnn.ipynb
│       ├── task3-hindi-cnn-bilstm.ipynb
│       └── task3_tamil_lstm_cnn.ipynb
├── dataset
│   ├── Additional_Data
│   │   ├── HASOC_data
│   │   ├── Hurtlex
│   │   └── MACD_data
│   ├── structure.txt
│   └── uli_dataset-main
│       ├── LICENSE
│       ├── README.md
│       ├── testing
│       └── training
├── final_codes
│   ├── TASK1
│   │   ├── fusion
│   │   ├── fusion_hurtlex
│   │   └── hurtlex
│   ├── TASK2
│   │   ├── fusion-hurtlex-english-task2.ipynb
│   │   ├── fusion-hurtlex-hindi-task2.ipynb
│   │   └── fusion-task2-tamil.ipynb
│   └── TASK3
│       ├── tamil-fusion-task3.ipynb
│       ├── task3-eng-fusion-hurtlex.ipynb
│       └── task3-hindi-fusion-hurtlex.ipynb
└── README.md


```