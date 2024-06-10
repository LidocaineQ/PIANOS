### PIANOS: Platform Independent and Normalization Free Single-sample Classifier

In this project, we developed PIANOS using a pathway-based k-TSP algorithm combined with resampling and ensemble modeling methods.

The model developed using the CIT cohort, offers prognostic risk stratification for individual colorectal cancer patients based on genetic sequencing data from any source. This model eliminates the constraints of pre-constructed cohorts and predefined cutoff values, providing a more flexible and precise approach to patient prognosis. The following figure describe the construction of PIANOS.

![image](https://github.com/LidocaineQ/PIANOS/blob/master/PIANOS.jpg)

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


## Model Construction
The model construction method is detailed in the file "model_construction.Rmd".

## Usage
The model usage instructions are detailed in the file "model_usage.Rmd".

### Data Description
The model's input consists of patients' gene expression data in the following format:
  
| sample | gene1 | gene2 | gene3 | ... | gene |
| --- | --- | --- | --- | --- | --- |
| patient | 5.15212166212432 | 2.88664048871183 | 5.3760491573249 | ... | 6.4355759773902 |
| patient | 4.94997883745515 | 2.37108757063653 | 5.0852982410145 | ... | 6.6052447056984 |
| ... | ... | ... | ... | ... | ... |
| patient | 5.22185205784889 | 2.20199502833056 | 5.3918173202651 | ... | 6.9666661456165 |
  
### Model Prediction
The model's output includes the patient's PIANOS score and stratification results.


### DEMO
We have uploaded the gene expression files of the publicly available ACICAM dataset along with the relevant code for usage, detailed in the file "DEMO.Rmd".
Source of public data: PMID: 37202560
