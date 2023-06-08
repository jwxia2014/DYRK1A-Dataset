# DYRK1A-Dataset

Introduction
-----------------------------------
DYRK1A-Dataset is the data set collected and curated for Machine Learning of DYRK1A molecules. 

Dataset Description
-----------------------------------
* DYRK1A_IC50_all.csv

   This file contains the DYRK1A molecules that were collected from ChEMBL29 database (https://www.ebi.ac.uk/chembl/) and curated by salt stripping, neutralization, SMILES standardization, the removal of compounds with too many rotatable bonds (>20) and too high molecular weight (>600) as well as the averaging of different IC50 values for the same compound. Please note the compounds with average IC50 below 1 μM were defined as active compounds and the others were defined as inactive compounds. [Wang Y. et al., CHINESE JOURNAL OF MEDICINAL GUIDE, 2022, 24(7): 672-677.]
   
   ![image](https://user-images.githubusercontent.com/50791273/232232990-094df7df-d6a2-4047-aac7-57a5b96c3e8d.png)


  
* DYRK1A_IC50_train.csv and DYRK1A_IC50_test.csv

   These two files contain the compounds in the training set (742 compounds) and those in the test set (185 compounds) by random partion.  

* MUBD_DYRK1A.csv  
   
   This file contains MUBD-DYRK1A (Maximal Biased Benchmarking Datasets for DYRK1A), which could be used for evaluating virtual screening strategies for DYRK1A inhibitors.  
   ![image](https://user-images.githubusercontent.com/50791273/232288177-41bb0398-d65d-414f-b1a4-a8fffa8ab237.png)


 
References
-----------------------------------
If you find the data sets useful, please cite: 

Si X.#, Wang Y.#, Qiu N.#, Qian C., Yao M., Wu S., Wang H.,* Zhang X.,* Xia J.*, Zhang L. Machine learning- and structure-based discovery of novel DYRK1A inhibitors for Alzheimer's disease. Bioorganic Chemistry,2023. submitted.
