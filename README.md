# assignment-5-Jerlinchellam12

Name : Jerlin Chellam J

Roll No: DA25C009

Documentation

# Visualizing Data Veracity Challenges in Multi-Label Classification

## Project Overview
This project explores **data veracity challenges** in multi-label classification using the Yeast gene expression dataset. Each data point represents an experiment with 103 gene expression features, and the target is a set of 14 functional categories (labels). Despite standardization, the dataset exhibits **noisy labels, outliers, and hard-to-learn samples**, which can hinder classification performance.

The main goal of this assignment is to **visually inspect the dataset** using **non-linear dimensionality reduction techniques** and understand how these data quality issues manifest in high-dimensional biological data.

## Objectives
- Apply **t-SNE** and **Isomap** to reduce feature dimensionality for visualization.  
- Identify and analyze:
  - **Noisy/Ambiguous Labels** – mislabeled or overlapping points.  
  - **Outliers** – isolated or unusual gene expression profiles.  
  - **Hard-to-Learn Samples** – points in highly mixed regions that challenge classifiers.  
- Compare **local vs. global structure preservation** between t-SNE and Isomap.  
- Understand the **manifold structure** and its impact on classification difficulty.

### **Part A: Preprocessing and Initial Setup**
**Description:**
1. **Data Loading:** Load the feature matrix (X) and multi-label target matrix (Y).  
2. **Dimensionality Check:** Report the number of features and data points.  
3. **Label Selection for Visualization:** Simplify 14 labels into key categories and “Other” for easier visualization.  
4. **Scaling:** Apply standardization to ensure distance-based methods like t-SNE and Isomap work correctly.

### **Part B: t-SNE and Veracity Inspection**
**Description:**
1. **t-SNE Implementation:** Reduce the scaled feature matrix to 2D, experiment with perplexity values to capture local neighborhoods.  
2. **Visualization:** Create 2D scatter plots colored by the simplified label index.  
3. **Veracity Inspection:** Identify noisy/ambiguous labels, outliers, and hard-to-learn regions to understand classifier challenges.

### **Part C: Isomap and Manifold Learning**
**Description:**
1. **Isomap Implementation:** Apply Isomap for 2D embeddings, preserving global data structure.  
2. **Visualization:** Generate scatter plots using the same coloring scheme as t-SNE for comparison.  
3. **Comparison and Curvature Analysis:**  
   - Compare t-SNE and Isomap to evaluate local vs. global structure preservation.  
   - Discuss manifold curvature and complexity, explaining why classification is challenging.

## Key Analyses
- **Preprocessing**: Scaling and simplified categorical coloring for visualization.  
- **t-SNE Visualization**: Captures local neighborhoods; highlights label mixing and noisy regions.  
- **Isomap Visualization**: Preserves global structure; reveals manifold curvature and multi-label overlaps.  
- **Manifold Curvature & Distance Preservation**: Quantitative assessment of classification difficulty and embedding quality.  
- **Intrinsic Dimensionality Analysis**: Scree plot, residual variance, and MLE estimates to determine the dataset’s effective dimensions (~8–12).

## Insights
- Multi-label gene expression data resides on a **curved, complex manifold**, causing classifier challenges.  
- **High-curvature regions** correlate with hard-to-learn samples.  
- Dimensionality reduction to 2D inevitably **loses class-separating information**, but helps understand **geometric and veracity challenges**.

## Tools & Libraries
- Python 3.x  
- NumPy, Pandas  
- Scikit-learn (t-SNE, Isomap)  
- Matplotlib, Seaborn
