# projet_phase2
#### Analyse de Données Cinématographiques

🎬 Movie Studio Strategic Analysis

**📋 Description du Projet**
Ce projet fournit une analyse data-driven complète pour guider les décisions stratégiques d'un nouveau studio de cinéma. L'analyse se base sur des données historiques de budgets et de performances de films pour identifier les stratégies de production les plus rentables.

## 🎯 Objectifs
Identifier la gamme de budget optimale pour maximiser le retour sur investissement (ROI)

Déterminer les périodes de sortie les plus propices

Analyser les tendances du marché cinématographique

Fournir des recommandations stratégiques actionnables

### 📊 Sources de Données
The Numbers Movie Budgets : Données complètes sur les budgets de production et les recettes mondiales

Période couverte : 2000 à aujourd'hui

Métriques inclues : budgets, recettes domestiques et mondiales, dates de sortie

# 🛠️ Technologies Utilisées
Python 3.x

Pandas - Manipulation et analyse des données

SQLite3 - Base de données relationnelle

Matplotlib & Seaborn - Visualisations

Jupyter Notebook - Environnement d'analyse

### 📁 Structure du Projet
text
movie-studio-analysis/
│
├── movie_analysis.db              # Base de données SQLite (générée automatiquement)
├── tn.movie_budgets.csv          # Données sources (à fournir)
├── movie_analysis.ipynb          # Notebook d'analyse principal
└── README.md                     # Documentation du projet
#### 🚀 Installation et Exécution
Prérequis
bash
pip install pandas numpy matplotlib seaborn jupyter sqlite3
Lancement de l'analyse
Télécharger les données :

Placez le fichier tn.movie_budgets.csv dans le répertoire du projet

Lancer Jupyter Notebook :

bash
jupyter notebook
Ouvrir et exécuter le notebook :

Ouvrez movie_analysis.ipynb

Exécutez les cellules dans l'ordre

Exécution alternative (script Python)
python
###  Si vous préférez exécuter directement
python -c "
import subprocess
subprocess.run(['jupyter', 'nbconvert', '--to', 'script', 'movie_analysis.ipynb'])
exec(open('movie_analysis.py').read())
"
### 📈 Méthodologie d'Analyse
1. Nettoyage des Données
Conversion des valeurs monétaires en format numérique

Filtrage des données aberrantes

Catégorisation par niveau de budget

**2. Métriques Calculées**
**Profit =** Recettes mondiales - Budget de production

**ROI =** (Profit / Budget de production) × 100

Taux de succès = Pourcentage de films rentables

### 3. Catégories de Budget
Petit Budget : < 20 millions $

Budget Moyen : 20-50 millions $

Gros Budget : 50-100 millions $

Blockbuster : > 100 millions $

### 💡 Résultats Clés
Stratégie Optimale Identifiée
Métrique	Valeur Recommandée
Catégorie de budget	Budget Moyen ($20-50M)
ROI moyen attendu	[Valeur à calculer]%
Meilleure période	[Mois identifié]
Taux de succès	[Valeur à calculer]%
Insights Principaux
Rentabilité par budget : Les films à budget moyen offrent le meilleur équilibre risque/rendement

Saisonnalité : Certains mois présentent un ROI significativement plus élevé

Taux de succès : Varie considérablement selon la catégorie de budget

# 🎬 Recommandations Stratégiques
***Phase 1 (Années 1-2)***
Focus : Productions à budget moyen ($20-50M)

Objectif : Établir une track record de succès

Sorties : Cibler les mois identifiés comme optimaux

***Phase 2 (Années 3-4)***
Expansion : Introduction de productions à gros budget

Diversification : Exploration de nouveaux genres

Partenariats : Développement de relations internationales

***Phase 3 (Année 5+)***
Maturation : Production de blockbusters sélectifs

Innovation : Investissement dans de nouvelles technologies

Marque : Établissement d'une identité studio distinctive

## 📊 Base de Données
Le projet utilise SQLite avec les tables suivantes :

**Tables Principales**
raw_movie_budgets : Données brutes importées

movies_clean : Données nettoyées et enrichies

analysis_report : Métriques et recommandations synthétiques

top_performers : Films les plus performants

****Exemple de Requêtes****
sql
-- Performance par catégorie de budget
SELECT budget_category, AVG(roi) as avg_roi, COUNT(*) as count
FROM movies_clean 
GROUP BY budget_category 
ORDER BY avg_roi DESC;

-- Top 10 des films les plus rentables
SELECT movie, release_year, production_budget, worldwide_gross, profit, roi
FROM movies_clean 
ORDER BY profit DESC 
LIMIT 10;
#### 📈 Visualisations Générées
Le notebook produit 6 visualisations clés :

ROI par catégorie de budget - Bar chart comparatif

Taux de succès par catégorie - Analyse du risque

Évolution des budgets - Tendances temporelles

Performance saisonnière - ROI par mois

Relation budget-profit - Scatter plot

Distribution des ROI - Histogramme

## 🔮 Perspectives Futures
Améliorations Possibles
Intégration de données de genres cinématographiques

Analyse des coûts marketing

Données de performance par territoire

Sentiment analysis des critiques

Données de streaming et VOD

Évolutions Technologiques
Dashboard interactif avec Streamlit

API de prédiction de performance

Intégration de données en temps réel

Machine learning pour la prédiction de succès

# 🤝 Contribution
Les contributions sont les bienvenues ! Voici comment participer :

Forkez le projet

Créez une branche pour votre fonctionnalité

Committez vos changements

Push vers la branche

Ouvrez une Pull Request

# 📝 Licence
Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

👥 Auteurs
Équipe d'Analyse Data - Analyse initiale et développement

Direction Studio - Définition des besoins stratégiques

📞 Support
Pour toute question ou problème :

Ouvrir une issue sur le repository

Contacter l'équipe data à data-jeffyscool141@gmail.com

 **💡 Citation de l'équipe**: "Dans le cinéma moderne, les données ne remplacent pas la créativité, mais elles éclairent les décisions qui permettent à la créativité de s'épanouir."

<div align="center">
Lights, Camera, Data! 🎥📊

</div>
