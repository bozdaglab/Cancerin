# Cancerin
Cancerin is a tool to infer genome-wide cancer-associated ceRNA interaction network in cancer.  

Scripts to run Cancerin are in **run_cancerin.R**. Required inputs for Cancerin include: 
* Four dataframes contains gene-level information of RNA and miRNA expression, copy number alteration, and DNA methylation. The corresponding variable names used in **run_DyCeR.R** are _mRNA_, _miRNA_, _cna_, and _methyl_. 
  - Each column in those dataframes refer to a tumor sample. 
  - Each row in the _RNA_, _cna_, and _methyl_ refers to RNA expression level, copy number, and methylation beta value of a differenitally expressed (DE) RNAs, respectively. Each row in _miRNA_ refers to the expression of a DE miRNA.  
* A dataframe named _tf.target.interactions_. Each row in _tf.target.interactions_ refers to a putative interaction between a transcription factor (TF) and a gene. 
* A dataframe named _miRNA.target.interactions_. Each row in _miRNA.target.interactions_ refers to a putative interaction between a miRNA and a gene. 
  
Sample input data for Cancerin could be found in _sampleData.rda_. 
