# Network Intrusion Detection System — CIC-IDS-2017

Progetto per il corso di Fondamenti di Artificial Intelligence. 
Pipeline completa di Machine Learning per la classificazione multiclasse del traffico di rete 
su dataset **CIC-IDS-2017** (Canadian Institute for Cybersecurity).

---

## Struttura del Progetto

```
CIC-IDS-2017/
├── notebooks/
│   ├── 01_dataloading_and_eda.ipynb
│   ├── 02_feature_engineering_selection.ipynb
│   └── 03_model_training_evaluation.ipynb
├── data/
│   └── raw/                        # CSV del dataset (consiglio di scaricare separatamente)
├── output/
│   ├── reports/                    # Report di EDA
│   ├── feature_analysis/           # Risultati analisi feature
│   ├── model_results/              # Metriche e CSV risultati
│   ├── images/              # Immagini per training e feature importance
│   └── eda_images/                 # Grafici EDA
└── requirements.txt
```

---

## Note Importanti sui Notebook

**I notebook sono distribuiti senza output.**  
Ogni notebook genera decine di immagini (distribuzioni, feature importance, ecc.). Includere gli output farebbe aumentare di molto la dimensioni dei file
rendendoli difficili da aprire con un editor.

**Usare Jupyter Web, non PyCharm.**  
L'esecuzione tramite PyCharm (personalmente) causa crash del sistema operativo.
Il training dei modelli ha richiesto 6+ ore sul mio hardware.
Anche la visualizzazione degli output viene tagliata su pycharm
e risulta molto pesante anche solo nella visualizzazione.

```bash
# Avviare con:
jupyter lab
```

---

## Attenzione alla Clone

La clone del repository potrebbe richiedere alcuni minuti a causa dei file come immagini ma soprattutto per il dataset

```bash
git clone https://github.com/emanuelep57/CIC-IDS-2017.git
cd CIC-IDS-2017
```

---

## Installazione

```bash
pip install -r requirements.txt
```

Librerie principali: `scikit-learn`, `lightgbm`, `tensorflow`,
`imbalanced-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `joblib`.

---

## Pipeline

Eseguire i notebook **in ordine**:

1. `01_dataloading_and_eda.ipynb` — carica i CSV, cleaning, label engineering (15→8 classi)
2. `02_feature_engineering_selection.ipynb` — ratio features, consensus ranking (79→20 feature), split 70/15/15
3. `03_model_training_evaluation.ipynb` — 5-fold CV, training 6 modelli, model selection, test finale

---

## Autore

Emanuele Pascale — Università degli Studi di Salerno, A.A. 2025/2026
