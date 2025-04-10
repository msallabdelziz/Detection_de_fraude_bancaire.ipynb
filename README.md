# Détection de fraude bancaire

# Description

Ce projet vise à détecter les transactions bancaires frauduleuses en combinant des techniques de machine learning et de deep learning. Il utilise un modèle Random Forest (classification supervisée) et un autoencodeur (détection d’anomalies non supervisée) pour identifier les fraudes. Le code est implémenté dans un notebook Jupyter et comprend le prétraitement des données, le rééquilibrage des classes avec SMOTE, ainsi que l’évaluation des performances à l’aide de rapports de classification, de la métrique AUC-ROC et de courbes ROC et Précision-Rappel.

Ce projet utilise le jeu de données « creditcard.csv » disponible sur Kaggle.

# Contenu

- Notebook Jupyter : Detection_de_fraude_bancaire.ipynb contenant l’ensemble du code du projet (prétraitement, entraînement des modèles, évaluation et visualisations).
- Prétraitement des données : Normalisation des variables temporelles et monétaires, et vérification de l’absence de valeurs manquantes.
- Déséquilibre des classes : Utilisation de la technique SMOTE pour sur-échantillonner la classe minoritaire (fraudes) et obtenir un ensemble d’entraînement équilibré.
- Modèle Random Forest : Entraînement d’un classifieur Random Forest sur les données d’entraînement équilibrées, suivi de la prédiction sur l’ensemble de test.
- Modèle Autoencodeur : Entraînement d’un autoencodeur (réseau de neurones) sur les transactions normales afin de détecter les transactions atypiques par erreur de reconstruction.
- Évaluation et visualisation : Génération d’un rapport de classification (précision, rappel, F1-score) pour évaluer chaque modèle, calcul de l’AUC-ROC, tracé de la courbe ROC et de la courbe Précision-Rappel pour visualiser les performances des modèles.

# Utilisation

1. Cloner le dépôt : Téléchargez ou clonez ce dépôt GitHub sur votre machine locale.
2. Installer les dépendances : Assurez-vous d’installer les bibliothèques Python requises, par exemple avec pip install -r requirements.txt si un fichier de requirements est fourni. Les principaux packages utilisés sont pandas, numpy, scikit-learn, imbalanced-learn (pour SMOTE), matplotlib, seaborn et tensorflow/keras (pour l’autoencodeur).
3. Obtenir les données : Téléchargez le jeu de données de transactions bancaires (fichier creditcard.csv) depuis la source Credit Card Fraud Detection sur Kaggle et placez-le dans le répertoire du projet.
4. Exécuter le notebook : Ouvrez le notebook Jupyter Detection_de_fraude_bancaire.ipynb à l’aide de Jupyter Notebook/Lab ou d’une plateforme comme Google Colab. Exécutez les cellules séquentiellement pour reproduire l’analyse.
5. Résultats : Le notebook affichera les métriques d’évaluation (rapport de classification, AUC, etc.) et les graphiques des courbes ROC et Précision-Rappel. Ces résultats permettront d’interpréter les performances du modèle Random Forest et de l’autoencodeur dans la détection de fraudes.

# Données
Les données utilisées proviennent d’un jeu de données public de transactions par carte de crédit. Ce jeu de données comporte 284 807 transactions effectuées sur deux jours, dont 492 sont frauduleuses (soit ~0,17%). Les variables explicatives sont entièrement numériques : 30 d’entre elles (V1 à V28, plus Time et Amount) représentent des caractéristiques transformées (les features V1–V28 proviennent d’une PCA effectuée pour anonymiser les informations sensibles, tandis que Time correspond au temps écoulé et Amount au montant de la transaction). La variable cible Class indique la nature de la transaction : 0 pour une transaction normale et 1 pour une transaction frauduleuse. Étant donné le déséquilibre extrême des classes, des techniques de rééchantillonnage comme SMOTE sont appliquées afin d’améliorer la capacité du modèle à détecter les fraudes.
Licence

Ce projet est distribué sous la licence MIT. Veuillez consulter le fichier LICENSE pour plus d’informations.