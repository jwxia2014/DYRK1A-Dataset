# DYRK1A-Dataset

Introduction
-----------------------------------
DYRK1A-Dataset is the data set collected and curated for Machine Learning of DYRK1A molecules. 

Dataset Description
-----------------------------------
1. The source 

 

Implementation
-----------------------------------
* Source

  ChEMBL29 database (https://www.ebi.ac.uk/chembl/)  
  
* Curation


1161 compounds with homo sapiens DYRK1A activity values (IC50) were downloaded from the ChEMBL29 database. RDKit (version 2019.09.3) and MolVS (version 0.1.1) were used to remove the salt components, neutralize the compounds and standardize SMILES representations. Compounds with too many rotatable bonds (>20) and too high molecular weight (>600) were removed. Only the compounds with clear IC50 values were extracted and the average value was used for  with more than one IC50 values. Compounds with biological activity values below 1 μM were defined as active compounds and others as inactive compounds. 
![image](https://user-images.githubusercontent.com/50791273/232232990-094df7df-d6a2-4047-aac7-57a5b96c3e8d.png)


  
3. Download 'xgboost-1.0.2-cp37-cp37m-win_amd64.whl' from https://www.lfd.uci.edu/~gohlke/pythonlibs/#xgboost
4. Create a new directory, e.g. D:/HDAC3i-Finder and put the file 'xgboost-1.0.2-cp37-cp37m-win_amd64.whl' in D:/HDAC3i-Finder  
5. Run 'Anaconda Prompt' and run the following commands:

   $ conda activate HDAC3
   
   $ pip install D:/HDAC3i-Finder/xgboost-1.0.2-cp37-cp37m-win_amd64.whl
   
   $ pip list | findstr xgboost (if 'xgboost 1.0.2' returns, xgboost is installed successfully) 

* Run HDAC3i-Finder
1. download HDAC3i-Finder.py and put it in a directory, e.g. D:/HDAC3i-Finder  
2. Run 'Anaconda Prompt' and run the following commands:

    $ conda activate HDAC3
  
    $ python D:/HDAC3i-Finder/HDAC3i-Finder.py (The GUI application will be shown)

Usage
-----------------------------------
* Single Compound mode

  This mode is used for predicting whether a single compound is active for HDAC3 or not.  
  1. click the 'load a model' to load the 'XGBoost_Morgan2.m' model and paste SMILES of a compound to predict. 
  2. click the 'Classify' button and the activity class of the compound is shown in the textbox along with the probability of the activity class. 

* A Set of Compounds mode (virtual screening)

  This mode is used for virtual screening of a large chemical library.  
  1. click the 'load a model' to load the 'XGBoost_Morgan2.m' model and provide a csv file with 'IDNUMBER' and 'SMILES' of the compounds to predict. 
  2. click the 'Classify' button and a csv file that contains activity classes with probability values of "being ACITVE" in a descending order returns.  

References
-----------------------------------
If you find HDAC3i-Finder useful, please cite: 

Li, S., Ding Y., Chen, M., Chen Y., Kirchmair J., Zhu Z., Wu, S., Xia, J.*, HDAC3i-Finder: A Machine Learning-based Computational Tool to Screen for HDAC3 Inhibitors. Mol. Inf.,2021, 40(3):e2000105. https://onlinelibrary.wiley.com/doi/10.1002/minf.202000105 (Top Cited Article 2020-2021 of Mol. Inf.)
