# Section 1

---

# **Single-cell transcriptomic data reveal T-cell subpopulations in primary and lymph node-metastatic gastric cancer**

# **1. Introduction**  

**Gastric cancer (GC)** is one of the most prevalent cancers worldwide, ranking as the fifth most common malignancy and the third leading cause of cancer-related deaths.

**Lymph node metastatic (LN) gastric cancer** represents a **critical stage** in **tumor progression**, where **lymph node involvement** significantly affects prognosis. 

This study conducts a **comprehensive analysis of T-cell subpopulations** in **primary and lymph node-metastatic gastric cancer**, focusing on their **functional heterogeneity** and **signaling pathways**.

---

# **2. Materials and Methods**  

## **2.1 Single-cell Dataset Sources**  
We obtained **single-cell RNA sequencing (scRNA-seq) data** from the **Gene Expression Omnibus (GEO)** database ([GSE163558](https://www.ncbi.nlm.nih.gov/geo/)). This dataset includes **primary gastric cancer (PT)** and **lymph node metastatic gastric cancer (LN)** samples. After filtering, we selected:  
- **Three PT samples**  
- **Two LN samples**  

## **2.2 Single-cell Data Analysis**  
Single-cell RNA sequencing data were processed using the *Seurat package* in R. The workflow included:  
1. **Quality Control**: Retained cells with mitochondrial gene percentage **< 10%** and gene count between **200 - 6000**.  
2. **Normalization & Scaling**: Used *SCTransform* function.  
3. **Dimensionality Reduction**: Applied *PCA* (first 20 components).  
4. **Batch Effect Correction**: Used *Harmony* package.  
5. **Clustering**: Identified cell types via *UMAP* and *FindClusters* functions.  
6. **Cell Type Annotation**: Based on *CellMarker 2.0*.

---

# **3. Results**  

## **3.1 Single-cell Landscape in PT and LN Samples**  
We identified **eight major cell types** through clustering and annotation:  *B cells*, *Endothelial cells*, *Fibroblasts*, *Mast cells*, *Myeloid cells*, *Neutrophil/Neural progenitor cells*, *NK cells* and *T cells*. 

The proportion of *T cells* was **higher in LN samples** compared to PT samples, whereas *Myeloid cells* were more abundant in **PT samples**.  

**Figure 1**: **Single-cell landscape in PT and LN samples**  
![UMAP of cell clusters](images/landscape.png)

## **3.2 T Cell Pathway Heterogeneity in PT and LN Samples**  
Pathway enrichment analysis revealed:  
- Upregulated in LN samples: *PI3K-Akt & IL-17* signaling pathways  
- Upregulated in PT samples: Protein Export pathway  

**Figure 2**: **Pathway enrichment of T cells**  
![Pathway enrichment](images/pathway.png)  

---

# Section 2

---

- How would you list all files in the current directory, including hidden ones?



