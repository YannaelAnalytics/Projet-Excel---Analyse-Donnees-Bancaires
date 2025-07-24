# 🔍 Analyse exploratoire – Fichier de travail Excel

Ce fichier contient l’ensemble des explorations effectuées à partir de la base de données initiale de Primero Bank.  
L’objectif est d’identifier des variables discriminantes pour comprendre les départs clients.

---

## 🛠 Méthodologie

- Une **feuille par variable** issue de la base (âge, revenu, type de carte, ancienneté, interactions, etc.)
- Un **tableau croisé dynamique (TCD)** est créé basé sur la base brute. On l'adapte en fonction de la variable étudiée, puis on le copie-colle dans la feuille d'étude de la variable.
- La variable analysée est ainsi **segmentée par tranche ou modalité**, en comparant systématiquement :
  - Les clients **actuels**
  - Les clients **partis**

🎯 But : repérer des écarts significatifs dans la répartition pour identifier des **profils à risque**.

---

## 📈 Démarche

1. **Création d’un TCD par variable**
2. **Segmentation pertinente** selon le type de variable (tranches, modalités, fourchettes)
3. **Analyse visuelle des écarts** entre les proportions de clients partis vs restants
4. **Interprétation des variables significatives** et élimination de celles peu utiles
5. **Croisement de certaines variables manuellement pour affiner le profil**

---

## ✅ Variables présentant un écart exploitable :

| Variable                | Observation clé |
|-------------------------|------------------|
| **Carte**               | Les clients avec carte **Platinum** sont très surreprésentés parmi les départs (on peut cependant nuancer par le fait que le nombre de cartes Platinum est très limité en comparaison avec le nombre de cartes bleues) |
| **Revenu**              | Les départs se concentrent chez les clients **revenus > 40K** |
| **Utilisation carte**   | 75 % des clients partis utilisent leur carte dans < 20 % de leurs dépenses |
| **Ancienneté**          | Pic de départ à **36 mois** d’ancienneté |
| **Interactions client** | La majorité des clients partis ont **1 à 3 interactions seulement** et la limite du nombre d'interactions des clients actuels est 5, au-delà on n'a que des clients partis |

---

## ⚠️ Variables **testées mais non discriminantes** :

Ces variables ont été explorées, mais **ne présentent pas d’écart significatif** entre les clients partis et restants, ou les écarts observés **ne justifient pas une segmentation stratégique** :

- **Genre** : répartition similaire hommes/femmes
- **Statut marital** : les mariés sont plus nombreux parmi les clients partis, mais aussi dans la base totale → **corrélation peu fiable**
- **Nombre de personnes à charge** : peu d’écarts significatifs

👉 Ces variables **n’ont pas été retenues dans la segmentation finale**, sauf si croisées avec d’autres.

---

## 📁 Fichier : `exploration/Projet PrimeroBank - Fichier de travail.xlsx`
