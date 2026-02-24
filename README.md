# Réseaux des détenteurs de sceaux byzantins : une analyse exploratoire sous Gephi

---

## 🎓 Contexte du Projet
Ce projet est réalisé dans le cadre du **Master 2 Langue et Informatique** à **Sorbonne Université** (Année universitaire 2025-2026). 

L'objectif est de modéliser et de visualiser les réseaux sociaux et sémantiques des détenteurs de sceaux byzantins en utilisant le logiciel **Gephi**, afin d'explorer les interactions entre individus, titres officiels, localisations et iconographies religieuses.

---

## 📖 Introduction du Corpus
Le projet s'appuie sur le catalogue sigillographique publié dans *Travaux et mémoires* (2017), comprenant **43 notices de sceaux** au format PDF. 

L'extraction et la structuration des données (noms, fonctions, lieux, icônes religieuses) ont permis de construire un réseau complexe composé de :
* **109 nœuds**
* **135 relations (liens)**

---

## 📁 Structure du Dépôt
* **`code/`** : Scripts Python utilisant `PyMuPDF` pour l'extraction de texte et la structuration des données.
* **`corpus/`** : Corpus original des notices de sceaux en PDF.
* **`csv/`** : Données structurées exportées (`nodes_final.csv` pour les nœuds et `edges_final.csv` pour les relations).
* **`projet final.gephi`** : Fichier projet Gephi complet avec les paramètres de spatialisation et les calculs statistiques.
* **`Présentation.pdf`** : Support de présentation détaillant la méthodologie et les résultats clés.

---

## 🛠️ Méthodologie et Aspects Techniques

### 1. Prétraitement des données
* **Extraction** : Conversion des PDF en données textuelles structurées via `PyMuPDF`.
* **Normalisation** : Désambiguïsation des titres et lieux, et classification des symboles religieux (ex: Saint Georges, Christ, Vierge).

### 2. Construction du réseau
* **Types de nœuds** : Personne, Titre/Fonction, Lieu, Religion.
* **Relations** : Liens typés tels que `Personne - Titre` ou `Personne - Religion`.

### 3. Analyse Visuelle et Statistique
* **Algorithme de spatialisation** : Utilisation de **Force Atlas 2**.
* **Indicateurs clés** :
    * Degré moyen : **2.58**
    * Composante connexe : **92%** des nœuds interconnectés.
    * Modularité : **0.672** (indiquant une forte structure en communautés).

---

## 🔍 Principales Découvertes
* **Le rôle des passerelles religieuses** : Les icônes religieuses présentent une **centralité d'intermédiarité (Betweenness Centrality)** très élevée, agissant comme des ponts sémantiques entre les différents officiers.
* **Concentration du pouvoir** : Le cœur du réseau est dominé par les titres administratifs (ex: *protospathaire*, *patrice*), reflétant la densité de la bureaucratie byzantine.
* **Structure communautaire** : La détection de communautés permet de distinguer des groupes socio-sémantiques tels que l'administration centrale, l'aristocratie militaire et les officiers provinciaux.



