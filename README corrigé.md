# 🎵 De l'oreille à l'algorithme — Classification des genres musicaux

**Un algorithme peut-il reconnaître un genre musical à partir de ses caractéristiques audio ?**
Ce projet entraîne un modèle de Machine Learning à distinguer cinq genres — **Afrobeat, Makossa, Bikutsi, Soul et Jazz** — à partir de cinq caractéristiques chiffrées : tempo, dansabilité, énergie, valence et acoustique.

## Contexte

Projet réalisé par **Alain Rodrigue Oyono**, Data Scientist certifié IBM et musicien professionnel (saxophoniste, 15 ans de scène). Il démontre un projet de données mené de bout en bout : création du jeu de données, entraînement d'un modèle, évaluation et prédiction — avec un atout qu'aucun jeu de données public ne fournit : les signatures des rythmes africains (Makossa, Bikutsi) sont définies à partir d'une oreille de musicien professionnel.

## Le jeu de données

- **60 morceaux, 12 par genre**, 5 caractéristiques audio par morceau (`data_africaine.csv`).
- Les plages de valeurs de chaque genre reflètent sa signature musicale réelle : Makossa très joyeux (valence élevée), Jazz très acoustique et peu dansant, Bikutsi rapide et très dansant, etc.
- **Transparence** : il s'agit d'un jeu de données de démonstration, construit par simulation à partir de cette expertise (graine aléatoire fixe, résultats reproductibles). L'étape suivante du projet est l'application du même pipeline à des données réelles (catalogue de titres étiquetés).

## Méthode

1. Génération et mélange du jeu de données (Pandas, NumPy), sauvegarde en CSV.
2. Séparation entraînement / test (80 % / 20 %, soit 48 / 12 morceaux).
3. Classificateur **Random Forest** (Scikit-Learn).
4. Évaluation : précision globale et rapport par genre, puis prédiction sur un morceau inconnu.

## Résultats

- **Précision globale : 83,3 %** sur les 12 morceaux de test.
- **Jazz et Soul : identifiés à 100 %** — leurs signatures sont les plus distinctes (acoustique élevée pour le Jazz, tempo lent pour la Soul).
- **L'Afrobeat est le genre le plus difficile** : ses voisins rythmiques (Makossa, Bikutsi) partagent tempo et énergie proches, et le modèle en classe une partie à côté — un résultat attendu, qui reflète une vraie proximité musicale.

## Technologies

- Python, Pandas, NumPy
- Scikit-Learn (Random Forest, métriques de classification)
- Jupyter Notebook

## Lancer le projet

```bash
pip install -r requirements.txt
jupyter notebook projet_music_data.ipynb
```

Exécuter les cellules de haut en bas : le notebook régénère le jeu de données, entraîne le modèle et affiche les résultats.

## Structure du dépôt

- `projet_music_data.ipynb` — le notebook complet (données, modèle, évaluation, prédiction)
- `data_africaine.csv` — le jeu de données (60 morceaux × 5 genres)
- `requirements.txt` — les dépendances Python

## Limites et pistes d'amélioration

- Jeu de données de démonstration et de petite taille : appliquer le pipeline à un catalogue réel et plus grand.
- Ajouter des caractéristiques (loudness, instrumentalness, speechiness) et une matrice de confusion visuelle.
- Comparer plusieurs modèles (Random Forest, XGBoost, régression logistique) et valider par validation croisée.
- Déployer une petite application de démonstration (Streamlit).

## Auteur

**Alain Rodrigue Oyono** — Data Scientist certifié IBM (2026) | Saxophoniste jazz / world / fusion
LinkedIn : [alain-oyono-9230a1230](https://www.linkedin.com/in/alain-oyono-9230a1230)
