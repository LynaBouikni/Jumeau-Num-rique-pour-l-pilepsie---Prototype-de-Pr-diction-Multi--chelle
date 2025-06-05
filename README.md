#  Jumeau Numérique pour l'Épilepsie — Projet Data Science de Bout en Bout

## 🎯 Objectif du projet

Ce projet vise à développer un **prototype de jumeau numérique personnalisé** pour les patients atteints d’épilepsie, capable de :

- Identifier les **variables associées à l’évolution de la maladie** à partir de données cliniques, EEG et génétiques
- Regrouper les patients par **profils cliniques** grâce à des méthodes de **machine learning non supervisées**
- Intégrer des **connaissances biomédicales externes** (ontologies, pharmacologie)
- Construire un **modèle prédictif multi-échelle** (clinique + EEG + expert)
- Fournir des **prédictions individualisées** via une interface prototype de jumeau numérique

---

## 🗂️ Contenu du projet

| Dossier/Fichier | Description |
|------------------|-------------|
| `data/`          | Données utilisées (open source ou simulées) |
| `notebooks/`     | Études exploratoires, PCA, clustering, modélisation |
| `src/`           | Scripts Python réutilisables (prétraitement, ontologie, modèles) |
| `models/`        | Modèles entraînés enregistrés (joblib/pkl) |
| `app/`           | Application Streamlit pour le jumeau numérique |
| `README.md`      | Ce fichier |
| `requirements.txt` | Environnement Python pour reproduire l’analyse |

---

## 🧪 Étapes réalisées

### 1. Analyse multivariée
- Exploration de données EEG et cliniques (UCI Epileptic Dataset)
- Réduction de dimension (PCA, UMAP)
- Corrélations entre variables cliniques et événements (crises, hospitalisation)

### 2. Machine Learning non supervisé
- Sélection de variables importantes (SHAP, LASSO)
- Clustering des patients (K-Means, DBSCAN)
- Identification de sous-groupes cliniques pertinents

### 3. Intégration de connaissances biomédicales
- Ontologie HPO intégrée via parsing `.obo`
- Graphe symptômes–gènes–traitements
- Enrichissement des données avec DrugBank et DisGeNET

### 4. Modélisation prédictive multi-échelle
- Fusion des données cliniques, EEG, et biomédicales
- Modèle supervisé (XGBoost, RandomForest)
- Prédictions : fréquence des crises, réponse au traitement, hospitalisations

### 5. Prototype de jumeau numérique
- Interface Streamlit interactive
- Saisie des variables patients
- Prédictions personnalisées + visualisation du "profil patient"

---

## 💡 Technologies utilisées

- **Langage** : Python 3.10+
- **Data Science** : pandas, numpy, matplotlib, seaborn
- **Machine Learning** : scikit-learn, XGBoost, SHAP
- **EEG / Signal** : MNE, pyEDFlib (facultatif)
- **Ontologies** : obonet, networkx
- **App web** : Streamlit
- **Survie (optionnel)** : lifelines

---

## 🔓 Données utilisées

- EEG transformé : [UCI Epileptic Seizure Recognition Dataset](https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition)
- Ontologie : [HPO – Human Phenotype Ontology](https://hpo.jax.org/app/download/ontology)
- Connaissances biomédicales : DrugBank, DisGeNET (via API)



---

## 🚀 Pour exécuter le projet

1. Cloner le repo :
```bash
git clone https://github.com/votre-utilisateur/epilepsy-digital-twin.git
cd epilepsy-digital-twin

