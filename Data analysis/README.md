This README is for MultidataSet_Analyer.py and Files_to_Deut.py


MultidataSet_Analyer.py

Original Author: Nate Zuniga
Modified by: Yi Jie (Josh) Tseng on 10/01/2023

Software requirement: Python
Python module requirement: scipy, sklearn, numpy, pandas and matplotlib


Purpose:
To perform normalization based on the Aguilan et al. 2020. It includes the following steps:
1. Clean and filter data.
2. log2 transformation, normalization with average, normalization of slope.
3. Separate the samples into groups for comparison and calculate the stats of those comparison.
4. Correct the -10logPV using Benjamini_Hochberg method.
5. Prepare the data for Ontology.
6. Plot volcano plots.
7. Convert the data format to DAVID compatible.


********************************* IMPORTANT IF RUNNING RNA DATA ****************************************

If running RNA data, the below softwares and modules are only required when you need to convert the gene ensembl
ID to UniprotID:

Softwares: chrome.exe, chromedriver.exe
Python modules: selenium, requests, bs4

Please note the version of your chrome.exe and use the corresponding version of chromedriver.exe
chromedriver.exe can be downloaded from https://googlechromelabs.github.io/chrome-for-testing/
Once chromedriver.exe is downloaded, place it in the same folder as this script.
****************************************** END ******************************************************

Useage:
For proteome data:
    python MultidataSet_analyzer.py -l <path_to_data_file_or_folder>
For RNAseq data:
    python MultidataSet_analyzer.py -l <path_to_data_file_or_folder> --RNA
If no need to convert data format for ontology for DAVID
    python MultidataSet_analyzer.py -l <path_to_data_file_or_folder> --convert False



--------------------------------------------------------------------------------------------------------


Files_to_Deut.py

Original Author: Nate Zuniga
Modified by Yi Jie(Josh) Tseng on 11/1/2023

This script is to convert the PEAKS11 output to PEAKS10 format which is compatible to deuterater.

Requirement:
Make sure to have the features.csv, protein.csv and peptide.csv from PEAKS11 output


Usage:

python Files_to_Deut.py -l <csv_file_location>