# Data-Comprehension-and-Visualization
The project serves as a practical application of fundamental data science concepts to real-world biomedical data, bridging theoretical knowledge with hands-on analytical experience. Students will gain proficiency in both computational analysis and scientific communication through their findings.
---

## 📌 **Objective**  
This practical work aims to analyze the separability of gene expression data from 5 types of cancer (BRCA, KIRC, COAD, LUAD, PRAD) using two approaches:  
1. **Quantitative method**: Measures of cohesion (intra-class distance) and separation (inter-class distance).  
2. **Visual method**: Dimensionality reduction (PCA, t-SNE) and visualization via histograms/scatter plots.  

---

## 📂 **Dataset**  
- **Source**: [RNA-Seq PANCAN (UCI)](https://archive.ics.uci.edu/dataset/401/gene+expression+cancer+rna+seq).  
- **Files**:  
  - `genomic_profiles.csv`: Patient × gene matrix (16,382 dimensions).  
  - `tumor_types.csv`: Cancer labels associated with each patient.  

---

## 🔍 **Methodology**  

### **1. Quantitative Approach**  
- **Calculated distances**:  
  - **Intra-class**: Maximum distance between a patient and their class center.  
  - **Inter-class**: Minimum distance between centers of two classes.  
- **Tested metrics**:  
  - Euclidean, Mahalanobis (subset of genes), Cosine.  
- **Indicator**:  
  - `Overlap(C₁, C₂) = (intra_dist(C₁) + intra_dist(C₂)) / (2 × inter_dist(C₁, C₂))`.  
  - If `Overlap < 1`: Well-separated classes.  

### **2. Visual Approach**  
- **Visualizations**:  
  - Histograms for 1-2 selected genes.  
  - Scatter plots colored by cancer type.  
- **Dimensionality reduction**:  
  - **PCA** (Principal Component Analysis).  
  - **t-SNE** (t-Distributed Stochastic Neighbor Embedding).  

---

## 📝 **Work Completed**  
### **Part 1: Without Visualization**  
1. Calculate `intra_dist` and `inter_dist` for all cancer pairs.  
2. Compare results using the 3 distance metrics (Euclidean, Mahalanobis, Cosine).  

### **Part 2: With Visualization**  
1. **Individual variables**:  
   - Display distributions by cancer type for 1-2 genes.  
2. **Scatter plots**:  
   - Before/after dimensionality reduction (PCA, t-SNE).  
3. **Joint distributions**:  
   - Visually compare cancer pairs.  

---
