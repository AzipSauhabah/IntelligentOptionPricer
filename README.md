# Pricer d’Options sur Indice (S&P 500) – Projet de Recrutement

## Objectif
🔥 **Objectif :** Évaluer la capacité du candidat à développer un pricer d’options européennes sur indice action (ex: S&P 500) en combinant plusieurs techniques avancées de finance quantitative et de programmation Python.

## Durée du projet
📅 **Durée du projet :** 1 week-end

## Objectifs Techniques
🚀 **Le projet doit démontrer la maîtrise des points suivants :**
- ✔️ Structuration et modularité du code (POO, gestion des erreurs, documentation)
- ✔️ Implémentation optimisée des modèles de pricing (Black-Scholes, Monte Carlo, Arbre Binomial)
- ✔️ Optimisation numérique (générateurs lazy, parallélisation, réduction de variance)
- ✔️ Récupération et interpolation des données de marché (Spot, Volatilité implicite, Courbe de taux)
- ✔️ Approximation du pricing par Machine Learning (réseau de neurones)
- ✔️ Comparaison des méthodes en précision et temps de calcul
- ✔️ Bonne gestion du projet avec Git et GitHub (structuration des commits, branches, PR)

⚠ **Ce projet est conçu pour être difficile afin que seul un candidat avec un solide bagage en finance quantitative et en programmation puisse le réussir.**

## 1. Implémentation des Modèles de Pricing
### 1.1 Black-Scholes (formule fermée)
- Implémentation sans bibliothèque spécialisée
- Gestion du taux de dividende
- Version vectorisée pour efficacité

### 1.2 Monte Carlo avec Optimisations
- Génération lazy (yield)
- Variables antithétiques, réduction de variance
- Matrice aléatoire pour approximer les Greeks
- Parallélisation (multiprocessing, concurrent.futures)
- Benchmark du temps de calcul

### 1.3 Arbre Binomial (Cox-Ross-Rubinstein)
- Implémentation récursive et vectorisée
- Gestion des dividendes continus
- Comparaison en précision et vitesse

## 2. Récupération des Données de Marché et Construction de la Courbe de Taux
### 2.1 Récupération du Spot et de la Volatilité
- Spot (S0) récupéré via API (yfinance, Alpha Vantage, etc.)
- Surface de volatilité implicite et interpolation bicubique

### 2.2 Construction de la Courbe de Taux sans Risque
- Récupération des taux US Treasury Bonds via API
- Interpolation spline cubique des taux zéro-coupon
- Implémentation avec QuantLib pour une courbe de discounting

## 3. Implémentation d’un Réseau de Neurones pour le Pricing
### 3.1 Données d’entraînement
- Entrées : (S0, K, r, σ, T, q)
- Sortie : Prix de l’option
- Dataset : 100 000 échantillons minimum
- Évaluation : RMSE entre ML et modèles analytiques

### 3.2 Architecture du Réseau
- MLP avec activation ReLU
- Optimisation Adam avec scheduler
- Comparaison des performances

## 4. Comparaison des Méthodes
| Méthode | Prix Option | Temps de Calcul (ms) | Erreur (%) |
|---------|-------------|----------------------|------------|
| Black-Scholes | 250.23 | 0.5 | 0.00% |
| Monte Carlo (1000 scénarios) | 249.80 | 120 | -0.17% |
| Monte Carlo (10000 scénarios) | 250.15 | 950 | -0.03% |
| Arbre Binomial (100 étapes) | 250.30 | 30 | +0.03% |
| Réseau de Neurones | 250.10 | 1.2 | -0.05% |

## 5. Organisation du Code et Bonnes Pratiques Git
### 5.1 Structure du Code
- 📌 `OptionPricer/` → Interface principale
- 📌 `MonteCarloPricer.py` → Simulation Monte Carlo optimisée
- 📌 `BlackScholesPricer.py` → Implémentation Black-Scholes
- 📌 `BinomialTreePricer.py` → Pricing par arbre binomial
- 📌 `RiskFreeCurve.py` → Gestion de la courbe de taux
- 📌 `VolatilitySurface.py` → Interpolation de la volatilité
- 📌 `NeuralNetworkPricer.py` → Approximation ML
- 📌 `Benchmarking.py` → Comparaison des méthodes

### 5.2 Exigences Git & GitHub
- ✅ Créer un repository GitHub public (sauf si déjà existant)
- ✅ Structurer les commits (pas de “fix bug” générique)
- ✅ Utiliser une branche `main` et au moins une branche `feature-X`
- ✅ Créer une Pull Request avant de fusionner `feature` dans `main`
- ✅ Ajouter un `.gitignore` pour exclure les fichiers inutiles
- ✅ Rédiger un README clair avec instructions d’exécution
- ✅ Publier le projet sur GitHub avec un rapport détaillé

## 6. Critères d’Évaluation
| Critère | Exigences |
|---------|-----------|
| Qualité du code | POO, documentation, structuration |
| Performance | Vectorisation, parallélisation |
| Précision des modèles | Comparaison rigoureuse |
| Python avancé | POO, programmation fonctionnelle, parallélisation |
| Machine Learning | Performance et précision |
| Utilisation des API | Récupération des taux et volatilités |
| Maîtrise de Git/GitHub | Structuration des commits et branches |

## 7. Consignes Finales
- 🔹 Le code doit être publié sur GitHub et bien documenté
- 🔹 Le projet doit être réalisé en autonomie sur un week-end
- 🔹 Un rapport explicatif détaillé est demandé

⚠ **Un bon code ne suffit pas : il faut être capable d’expliquer ses choix et de comparer les méthodes.**

🚀 **Bonne chance !**
