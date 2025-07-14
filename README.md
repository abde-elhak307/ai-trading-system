# Système de Trading Intelligent basé sur le Sentiment et les Données Boursières

Ce projet propose un système de trading intelligent qui combine l’analyse de sentiment et les données boursières pour prédire les tendances du marché à l’aide de modèles d’Apprentissage Automatique (ML) et d’Apprentissage Profond (DL).

## Structure du projet

```
project/
│
├── data/                # Données boursières et résultats
│   ├── ML_data/         # Données pour les modèles ML
│   ├── DL_data/         # Données pour les modèles DL
│   ├── model_metrics/   # Résultats des métriques des modèles
│   ├── model_summaries/ # Résumés des modèles
│   └── *.csv            # Fichiers de données brutes
│
├── ML/
│   └── data_preparation_and_ML_models.ipynb  # Notebook pour les modèles ML
│
├── DL/
│   └── DL_V4.ipynb      # Notebook pour les modèles DL
│
└── README.md            # Ce fichier
```

---

## Prérequis

Avant de commencer, assurez-vous d'avoir :

- **Python 3.7 ou supérieur**
  - Téléchargez-le depuis [python.org](https://www.python.org/downloads/)
  - Vérifiez l'installation avec :
    ```bash
    python --version
    ```

- **Jupyter Notebook**
  - Installez-le avec :
    ```bash
    pip install notebook
    ```
  - Lancez-le dans le dossier du projet avec :
    ```bash
    jupyter notebook
    ```

- **Bibliothèques Python nécessaires** :
  - pandas
  - numpy
  - scikit-learn
  - xgboost
  - tensorflow (pour Deep Learning)
  - keras (si séparé de tensorflow)
  - matplotlib
  - (optionnel) seaborn, tqdm, etc.

- **Installation rapide des dépendances** :
  - Installez toutes les bibliothèques d'un coup :
    ```bash
    pip install pandas numpy scikit-learn xgboost tensorflow matplotlib seaborn tqdm
    ```
  - Si un fichier `requirements.txt` est fourni, utilisez :
    ```bash
    pip install -r requirements.txt
    ```

---

## Utilisation des modèles ML

1. **Préparation des données**
   - Les données pour les modèles ML se trouvent dans `data/ML_data/`.
   - Les fichiers `all_train.csv` et `all_test.csv` contiennent les ensembles d’entraînement et de test.

2. **Lancement du notebook**
   - Ouvrez `ML/data_preparation_and_ML_models.ipynb` avec Jupyter Notebook.
   - Exécutez les cellules dans l’ordre pour :
     - Charger et préparer les données
     - Entraîner les modèles (KNN, RandomForest, SVR, XGBoost, etc.)
     - Évaluer les performances et sauvegarder les résultats dans `data/model_metrics/` et `data/model_summaries/`

---

## Utilisation des modèles DL

1. **Préparation des données**
   - Les données pour les modèles DL se trouvent dans `data/DL_data/`.
   - Les fichiers `all_train1.csv`, `all_val1.csv`, `all_test1.csv` sont utilisés pour l’entraînement, la validation et le test.

2. **Lancement du notebook**
   - Ouvrez `DL/DL_V4.ipynb` avec Jupyter Notebook.
   - Exécutez les cellules pour :
     - Charger et préparer les données
     - Construire et entraîner les modèles de Deep Learning (LSTM, GRU, etc.)
     - Évaluer les performances et sauvegarder les résultats

---

## Intégration des données

- Pour ajouter de nouvelles données boursières, placez les fichiers CSV dans le dossier `data/`.
- Mettez à jour les scripts ou notebooks pour pointer vers les nouveaux fichiers si nécessaire.
- Assurez-vous que le format des données (colonnes, types) correspond à celui attendu par les notebooks.

---

