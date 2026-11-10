🎵 De l'oreille à l'alarme : Classification des genres musicaux

🎯 Contexte du projet

Ce projet a été réalisé dans le cadre d'une candidature à un poste en Data Science. L'objectif est de démontrer la capacité à mener un projet de bout en bout : de la création du jeu de données jusqu'à l'entraînement et l'évaluation d'un modèle de Machine Learning.

💡 L'idée

Est-il possible pour un algorithme de reconnaître le genre musical d'un morceau (Afrobeat, Makossa, Bikutsi, Soul, Jazz) uniquement à partir de données chiffrées (tempo, énergie, dansabilité) ? Oui ! Ce projet prouve que l'on peut classifier la musique africaine et le jazz à partir de caractéristiques audio extraites et analysées via Python.

🛠️ Technologies utilisées

Langage : Python
Manipulation de données : Pandas, NumPy
Visualisation des données : Matplotlib, Seaborn
Machine Learning : Scikit-Learn (classificateur Forêt Aléatoire)
📊 Résultats obtenus

Le modèle de Machine Learning (Random Forest) atteint une précision de 83,3 % sur les données de test.

Le modèle est parfait (100 % de précision) pour identifier le Jazz (grâce à ses caractéristiques acoustiques spécifiques) et la Soul.
Il distingue l'Afrobeat du Bikutsi, qui partagent des tempos et une énergie similaires.
Le projet inclut une phase de prédiction sur un morceau « imaginaire » pour tester le modèle en conditions réelles.
🚀 Lancement du projet

Installer les dépendances :
BASH

pip install pandas numpy matplotlib seaborn scikit-learn jupyter
Ouvrir Jupyter Notebook :
BASH

jupyter notebook
Ouvrir le fichier projet_music_data.ipynb et exécuter les cellules jusqu'en bas.

