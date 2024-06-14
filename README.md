### PIANOS: Platform Independent and Normalization Free Single-sample Classifier

In this project, we developed PIANOS using a pathway-based k-TSP algorithm combined with resampling and ensemble modeling methods.

The model developed using the CIT cohort, offers prognostic risk stratification for individual colorectal cancer patients based on genetic sequencing data from any source. This model eliminates the constraints of pre-constructed cohorts and predefined cutoff values, providing a more flexible and precise approach to patient prognosis. The following figure describe the construction of PIANOS.

![image](https://github.com/LidocaineQ/PIANOS/blob/master/PIANOS.jpg)

Given the differences in training cohorts and labels, our method has the potential for broader application across various tumor types, enhancing its utility and effectiveness in diverse oncological contexts.

## Requirements

```
R 4.3.1
survival
gaofenglib
ggplot2
switchBox
tidyverse
DeepCC
```
```
install.packages("survival")
install.packages("ggplot2")
install.packages("tidyverse")

install.packages("BiocManager")
BiocManager::install("switchBox")
BiocManager::install("org.Hs.eg.db")

install.packages("devtools")
devtools::install_github("gflab/gfplot")
devtools::install_github("gaofeng21cn/gaofenglib")
devtools::install_github("CityUHK-CompBio/DeepCC")
```

## Model Construction
The model construction method is detailed in the file "model_construction.Rmd".

## Usage
The model usage instructions are detailed in the file "model_usage.Rmd".

### Data Description
The model input is an 𝑛 × 𝑘 gene expression matrix. An example format is shown below:
  
|  | gene1 | gene2 | gene3 | ... | gene |
| --- | --- | --- | --- | --- | --- |
| patient 1 | 5.15212166212432 | 2.88664048871183 | 5.3760491573249 | ... | 6.4355759773902 |
| patient 2 | 4.94997883745515 | 2.37108757063653 | 5.0852982410145 | ... | 6.6052447056984 |
| ... | ... | ... | ... | ... | ... |
| patient n | 5.22185205784889 | 2.20199502833056 | 5.3918173202651 | ... | 6.9666661456165 |
  
### Model Prediction
The model's output includes the patient's PIANOS score and stratification results.


### DEMO
We have uploaded the gene expression files of the publicly available ACICAM dataset along with the relevant code for usage, detailed in the file "DEMO.Rmd".
Source of public data: PMID: 37202560
