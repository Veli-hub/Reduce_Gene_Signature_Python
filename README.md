# Reduce_Gene_Signature_Python

Info: During my internship at the Institute for Experimental Oncology at the Universitätsklinikum Bonn my task was to implement a way of reducing a gene signature that still has predictive power over patient outcome. There are several papers that found gene signatures that can be used to predict immunotherapy success e.g.:
* Cancer Immunol Res July 1 2019 (7) (7) 1162-1174; DOI: 10.1158/2326-6066.CIR-18-0500: _A Gene Signature Predicting Natural Killer Cell Infiltration and Improved Survival in Melanoma Patients_
* Liao, M., Zeng, F., Li, Y. et al.: _A novel predictive model incorporating immune-related gene signatures for overall survival in melanoma patients. Sci Rep 10, 12462 (2020)._ https://doi.org/10.1038/s41598-020-69330-2 
* Aging (Albany NY). 2020 Jan 15; 12(1): 767–783. Published online 2020 Jan 12. doi: 10.18632/aging.102655: _Six-gene signature for predicting survival in patients with head and neck squamous cell carcinoma_ <a/>

We assume that a gene signature is given which has already predictive power so we can group patients by immune-high and immune low groups so that we can compare the groups of patients to the grouping using a smaller gene signature. Otherwise, one can also just give a initial grouping as input and compare it to the grouping determined by using the new gene signature. 
To compare two groupings of patients in immune-high and immune-low groups using different gene signatures, I use the Jaccard Index. Other Possibilities are: 
## Why do we do this? Possible uses:
We find that some genes are highly correlated, either positive or negative, and therefore using two highly correlated genes will not help us in our predicition that much. A shorter gene signature would be easier and more cost efficient to check so that before doing expensive procedures, one could assign patients to immune high or immune low groups. Other uses and benefits: 
* since there are different gene signatures already, one could try to improve those
* verify results using different data sets 
* usable on different cancer types and datasets
### What functions do we need? 
Python packages used: 

#### Different ideas
* Item 1
* Item 2
  * Item 2a
  * Item 2b
  
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
