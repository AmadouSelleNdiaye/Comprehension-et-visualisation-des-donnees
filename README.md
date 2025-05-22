# Comprehension-et-visualisation-des-donnees

---

## 📌 **Objectif**  
Ce travail pratique vise à analyser la séparabilité des données d'expression génétique de 5 types de cancers (BRCA, KIRC, COAD, LUAD, PRAD) à l'aide de deux approches :  
1. **Méthode quantitative** : Mesures de cohésion (distance intra-classe) et séparation (distance inter-classe).  
2. **Méthode visuelle** : Réduction de dimension (ACP, t-SNE) et visualisation par histogrammes/nuages de points.  

---

## 📂 **Jeu de Données**  
- **Source** : [RNA-Seq PANCAN (UCI)](https://archive.ics.uci.edu/dataset/401/gene+expression+cancer+rna+seq).  
- **Fichiers** :  
  - `profils_genomiques.csv` : Matrice patients × gènes (16 382 dimensions).  
  - `types_tumeurs.csv` : Labels des cancers associés à chaque patient.  

---

## 🔍 **Méthodologie**  

### **1. Approche Quantitative**  
- **Distances calculées** :  
  - **Intra-classe** : Distance maximale entre un patient et le centre de sa classe.  
  - **Inter-classe** : Distance minimale entre les centres de deux classes.  
- **Métriques testées** :  
  - Euclidienne, Mahalanobis (sous-ensemble de gènes), Cosinus.  
- **Indicateur** :  
  - `Overlap(C₁, C₂) = (dist_intra(C₁) + dist_intra(C₂)) / (2 × dist_inter(C₁, C₂))`.  
  - Si `Overlap < 1` : Classes bien séparées.  

### **2. Approche Visuelle**  
- **Visualisations** :  
  - Histogrammes pour 1-2 gènes sélectionnés.  
  - Nuages de points colorés par type de cancer.  
- **Réduction de dimension** :  
  - **ACP** (Analyse en Composantes Principales).  
  - **t-SNE** (t-Distributed Stochastic Neighbor Embedding).  

---

## 📝 **Travail Réalisé**  
### **Partie 1 : Sans Visualisation**  
1. Calculer `dist_intra` et `dist_inter` pour toutes les paires de cancers.  
2. Comparer les résultats avec les 3 distances (Euclidienne, Mahalanobis, Cosinus).  

### **Partie 2 : Avec Visualisation**  
1. **Variables individuelles** :  
   - Afficher les distributions par cancer pour 1-2 gènes.  
2. **Nuages de points** :  
   - Avant/après réduction de dimension (ACP, t-SNE).  
3. **Distributions conjointes** :  
   - Comparer visuellement les paires de cancers.  

---
