#PIANOS: Platform Independent and Normalization Free Single-sample Classifier

In this project, we developed PIANOS using a pathway-based k-TSP algorithm combined with resampling and ensemble modeling methods.

The model can robustly stratify colorectal cancer patients based on their risk of tumor recurrence.


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

## Usage：
The model usage instructions are detailed in the file "model_usage.Rmd".

### Data Description：
The model's input consists of patients' gene expression data in the following format:

    sample| Gene1 | Gene2 | Gene3 | ... 
    --- | --- | --- | --- | --- 
    Patient 1 |expression | expression | expression | ... 
    Patient 2 |expression | expression | expression | ... 
    ... | ... |	... | ... |	... 

### Model Prediction：
The model's output includes the patient's PIANOS score and stratification results.
