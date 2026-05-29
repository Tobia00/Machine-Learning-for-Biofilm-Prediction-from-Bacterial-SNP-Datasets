Machine Learning for Phenotype Prediction from SNP-Based GWAS Data
You can find in here a simple brief on how to interact with the mentioned Tool.

Features
Genomes annotation using Snippy
Data preprocessing
Feature filtering using MAF and variance thresholds
Model training using:
Decision Tree with hyperparameter tuning
SVM (Linear and RBF kernals)
Model evaluation:
Accuracy, Precision, Recall, F1-score
Confusion matrix
5-fold stratified cross validation
optional SMOTE for imbalanced phenotype classes
Extraction of the most informative SNPs
Optional Epsitasis detection through BLINK
Tool introduction:
1- GWAS and Epistasis Analysis
All isolates are processed using Snippy to provide a file that will have all the SNPs relative to the reference genome and the type of bacteria used as input then snippy core to extract shared variables genomic positions and make the core.vcf file the file can be used as direct input for the ML model or check the epistatic interactions between SNPs using BLINK module
2- Machine Learning Pipeline
Preprocessing for the core.vcf file by transposing the file to make it compatible for the model and ensuring the data is numeric. Feature filtering and extraction, then the data is split into 80% training and 20% testing with stratification then two models are used DT and SVM. Hyperparameter tuning via GridSearchCV is done and at the end evaluation using the metrics accuracy, precision, recall, F1-score, and visualization of the confusion matrix
Requirements:
numpy==2.1.1
pandas==2.2.3
scikit-learn==1.5.2
imbalanced-learn==0.12.4
joblib==1.4.2
matplotlib==3.9.2
cyvcf2==0.31.1
pyyaml==6.0.2
Conda==25.11.1
Snippy==4.3.6
Plink==2
Python==3.14,3.10
Input files:
Core.vcf – multi-sample SNP genotype file.
phenotype.csv

epistasis_features.csv – SNP–SNP interaction features.
Contact Info
s-ahmed.eid@zewailcity.edu.eg
s-Haitham.mohamed@zewailciy.edu.eg
