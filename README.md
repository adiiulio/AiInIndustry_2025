# AI Fairness Analysis
## AI in Industry project and project work

The aim of this project is to study the fairness of the hiring process in the context of the Adecco company. This is a topic which is extremely relevant in today's world, as the increase usage of AI in such fields is raising concerns, and it is important to verify the fairness of the models to ensure that the process is conducted correctly and with as little bias as possible.

We decided to implement techniques found in articles and studied in class to perform this task.

The dataset is split into two parts: direct matching (contains best 10 candidates for each position) and reverse matching (contains best positions for each candidate). The two cases are handled in the two different notebooks. 


## Updated Version
Bias Detection in Matching Datasets
The aim of this project is to study the fairness of the hiring process in the context of the Adecco company. This is a topic which is extremely relevant in today's world, as the increase usage of AI in such fields is raising concerns, and it is important to verify the fairness of the models to ensure that the process is conducted correctly and with as little bias as possible.

We decided to implement techniques found in articles and studied in class to perform this task.

This project explores bias detection in two structurally related datasets — Direct Matching and Reverse Matching — using a combination of statistical distribution-based techniques and fairness toolkits. The goal is to evaluate how different bias detection methods perform across datasets with varying characteristics.

### Project Structure
direct_matching.ipynb:
Investigates the Direct Matching Dataset, where certain types of bias are only detectable using distributional techniques such as:

Jensen-Shannon Divergence (JSD)

Kullback-Leibler (KL) Divergence

Wasserstein Distance

These methods uncovered subtle biases that were not detected by fairness toolkits like FairLearn and AIF360, which focus primarily on group-level metrics.

Reverse_Matching.ipynb:
Applies the same set of techniques to the Reverse Matching Dataset.
In this case, all techniques aligned, consistently detecting bias related to domicile region, while finding little to no bias in features such as gender and age.
This highlights how bias can be more apparent in some datasets and emphasizes the importance of method selection.

### Techniques Used
- Distributional Techniques
KL Divergence

Jensen-Shannon Divergence

Wasserstein Distance
These techniques evaluate distributional shifts and are capable of detecting individual- or subgroup-level disparities that may be missed by traditional fairness metrics.

- Fairness Toolkits
AIF360

FairLearn
Used to assess bias through group-level fairness metrics, such as:

Demographic Parity


### Key Findings
In the Direct Matching Dataset, only distributional techniques revealed hidden biases.

In the Reverse Matching Dataset, all methods agreed that domicile region was a biased feature, while gender and age showed no meaningful bias.

The results underscore the importance of applying multiple bias detection methods to gain a full understanding of fairness in machine learning pipelines.

### Requirements
Python 3.x

scikit-learn

fairlearn

aif360

scipy

pandas, numpy, matplotlib, seaborn
