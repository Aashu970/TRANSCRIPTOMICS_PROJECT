# 🧬 Transcriptomics Project: TCGA-BRCA RNA-seq Analysis

## 📖 Introduction
This project focuses on large-scale transcriptomic analysis of **TCGA-BRCA RNA-seq counts** combined with clinical metadata.  
The goal is to identify differentially expressed genes (DEGs), construct co-expression networks, apply machine learning for classification, and derive a prognostic hub gene signature relevant to breast cancer survival outcomes.

---

## ⚙️ Workflow

### 1. Heavy Data Processing
- Input: TCGA-BRCA RNA-seq counts + clinical metadata  
- Steps: data cleaning, sample filtering, normalization, batch effect evaluation  
- Visualization: PCA plots before and after filtering  
- Tools: FastQC, MultiQC, R (edgeR/DESeq2), Python (pandas, matplotlib, seaborn)

### 2. Differential Expression Analysis
- Identify DEGs using DESeq2/edgeR  
- Biological interpretation: cell cycle activation, DNA repair dysregulation, estrogen signaling  
- Visualization: volcano plots, heatmaps  
- Tools: R/Bioconductor, Python (statsmodels, scikit-learn)

### 3. Weighted Gene Co-expression Network (WGCNA)
- Build gene modules and study relation between modules and traits  
- Focus: co-regulated pathways and systems-level organization  
- Tools: WGCNA (R), Cytoscape, Python (networkx, py2cytoscape)

### 4. Machine Learning
- Train/test split: 70/30  
- Algorithms: Random Forest, XGBoost  
- Metrics: ROC-AUC, precision, recall, F1 score  
- Feature selection: genes consistently associated with tumor status  
- Tools: Python (scikit-learn, XGBoost)

### 5. Survival Analysis
- Kaplan-Meier curves and Cox regression using TCGA clinical data  
- Multivariate Cox analysis for clinical relevance  
- Tools: R (survival, survminer), Python (lifelines)

### 6. Final Hub Gene Signature
- Integration of DEGs, WGCNA hubs, PPI hubs, ML-important genes  
- Build a 5–10 gene prognostic signature  
- Determine patient risk scores and classify survival outcomes  
- Tools: Cytoscape (STRING PPI), Python (networkx, lifelines)

---

## 📈 Key Outcomes
- Identification of breast cancer DEGs with functional relevance  
- Gene co-expression modules linked to clinical traits  
- Machine learning models achieving strong predictive performance (ROC-AUC, F1 score)  
- Survival analysis highlighting clinically relevant gene sets  
- Final hub gene signature (5–10 genes) for patient risk stratification

---

## 🔁 Reproducibility
- Download TCGA-BRCA RNA-seq counts and clinical metadata  
- Perform preprocessing with FastQC/MultiQC and normalization in R  
- Run DEG analysis with DESeq2/edgeR  
- Construct WGCNA modules and visualize in Cytoscape  
- Train ML models in Python (scikit-learn, XGBoost)  
- Conduct survival analysis in R/Python  
- Integrate results to derive hub gene signature  
