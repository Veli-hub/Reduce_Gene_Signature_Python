# Reducing A Gene Signature Using Python

Info: During my internship at the Institute for Experimental Oncology at the Universitätsklinikum Bonn my task was to implement a way of reducing a gene signature that still has predictive power over patient outcome for immunotherapy. There are several papers that found gene signatures that can be used to predict immunotherapy success e.g.:
* Cancer Immunol Res July 1 2019 (7) (7) 1162-1174; DOI: 10.1158/2326-6066.CIR-18-0500: _A Gene Signature Predicting Natural Killer Cell Infiltration and Improved Survival in Melanoma Patients_
* Liao, M., Zeng, F., Li, Y. et al.: _A novel predictive model incorporating immune-related gene signatures for overall survival in melanoma patients. Sci Rep 10, 12462 (2020)._ https://doi.org/10.1038/s41598-020-69330-2 
* Aging (Albany NY). 2020 Jan 15; 12(1): 767–783. Published online 2020 Jan 12. doi: 10.18632/aging.102655: _Six-gene signature for predicting survival in patients with head and neck squamous cell carcinoma_ <a/>

We assume that a gene signature is given which has already predictive power so we can group patients by high-susceptible and low-susceptible groups so that we can compare the groups of patients to the grouping using a smaller gene signature. Otherwise, one can also just give a initial grouping as input and compare it to the grouping determined by using the new gene signature. 
To compare two groupings of patients in immune-high and immune-low groups using different gene signatures, I use the Jaccard Index. Other Possibilities could be implemented.  
## Why do we do this? Possible uses:
We find that some genes are highly correlated, either positive or negative, and therefore using two highly correlated genes will not help us in our predicition that much. Other features dont hold important information about patient outcome and can therefore be dropped. A shorter gene signature would be easier and more cost efficient to check so that before doing expensive procedures, one could assign patients to groups which react good to immuntherapy and those who react badly. Other uses and benefits: 
* since there are different gene signatures already, one could try to reduce those
* verify results using different data sets 
* usable on different cancer types and datasets
* visualisations are easier to understand
### What functions do we need? 
Python packages used: 

#### Feature Selection
To get the best predictor of patient outcome of a given size k from a set of genes of size n, one would have to check k choose n combinations of genes. Brute Forcing through every combination is computationally too hard, so we use different methods that are less costly. Algorithms that could be used: Recursive Feature Elimination, Forward Feature Selection, PCA, Brute Force on a small set for the best two gene signature (only have to compare n chose 2 different combinations), RFECV Redundant Feature Elimnation with cross validation find optimal number of features

#### Input 
As input we have: 
* patient/sample data
* associated therapy survival data
* initial gene signature
* Jaccard Index threshhold
* p-Value threshhold
* (ground truth grouping
if wanted)
* depending on the algorithms used and desired worlflow
#### Functions
Classification, singscore, the different methods, correlation, kaplan meier log rank p value
#### Output
A gene signature, Kaplan Meier curve with confidence intervalls, p value, jaccard index or other metric for comparing classification, heat map correlation, abs number of people in wrong groups and in right groups each individually
#### Tutorial
Regarding the use of this classification, to examine wether someone gets treated with immunetherapy or not, we really dont want any misclassification in some cases. This might lead to wrong decision making in cancer treatment, even though this is not the only parameter checked for obviously. Because of that either penalize wrong classification in the extremes or use high treshhold for jaccard index atleast. \
cross validation



* Item 1
* Item 2
  * Item 2a
  * Item 2b
  
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
