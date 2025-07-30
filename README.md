# gMBA: Expression Semantic Guided Mixed Boolean-Arithmetic Deobfuscation

This repository contains the official implementation and dataset for the paper:

## 📄 **paper**

> **gMBA: Expression Semantic Guided Mixed Boolean-Arithmetic Deobfuscation Using Transformer Architectures**  
> [Accepted at Findings of ACL2025]  

## 🔍 Overview

Mixed Boolean-Arithmetic (MBA) expressions are widely used in software obfuscation to hinder reverse engineering and malware analysis.  
**gMBA** presents a novel Transformer-based sequence-to-sequence model that deciphers obfuscated MBA expressions into their simplified forms.

Unlike prior approaches, gMBA leverages:
- **Semantic** features from the expression via automatically constructed **truth tables**
- A lightweight yet expressive **Transformer architecture** guided by these semantics


## ⁉️ How to use

```
git clone https://github.com/your-username/gMBA.git
cd gMBA
pip install -r requirements.txt
```

You may need to install torch series by the commands below
```
pip install torch==2.0.0+cu117 -f  https://download.pytorch.org/whl/torch_stable.html

pip install torchtext==0.6.0 -f https://download.pytorch.org/whl/torch_stable.html

pip install torchdata==0.6.0 -f https://download.pytorch.org/whl/torch_stable.html
```

Then just run your notebook files!


<!-- ## 📖 Citation
If you find this repository helpful, please cite our paper:
```
``` -->

## 📂 Project Structure

```bash
.
├── data/
│   ├── train_s.csv
│   ├── train_s-bool_tt_added.csv
│   ├── train_s-arith_tt_added.csv
│   ├── train_s-both_tt_added.csv
│   ├── test.csv
│   ├── test-bool_tt_added.csv
│   ├── test-arith_tt_added.csv
│   └── test-both_tt_added.csv
│
├── baseline/
│   ├── transformer_baseline.py
│   └── ...
│
├── addition/
│   ├── transformer_add.ipynb
│   └── ...
├── concat_token/
│   ├── transformer_cat_tok.ipynb
│   └── ...
├── concat_hiddim/
│   ├── transformer_cat_hiddim.ipynb
│   └── ...
│
├── README.md
└── requirements.txt
```