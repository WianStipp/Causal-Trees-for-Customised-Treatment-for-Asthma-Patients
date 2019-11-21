# Causal Trees for Customised Treatment for Asthma Patients
 A study to compare the quality of services provided by two physician groups for asthma patients.
### Describing The Problem:

We are using a study to compare the quality of services provided by two physician groups for asthma patients in California. Let $Y_i(z)$ be the score (1 = satisfactory, 0 = non-satisfactory) given by patient $i$ for the treatment recieved by physician  group $z \in \{1,2\}$ 
Besides the treatment variable and the outcome variable we have a list of covariates: 'age', 'sex', 'education', 'insurance', 'drug coverage', 'severity', 'comorbidity', 'physical comorbidity', 'mental comorbidity'.

Comorbidity is defined as: the presence of one or more additional conditions co-occurring with a primary condition; in the countable sense of the term, a comorbidity is each additional condition. The additional condition may also be a behavioral or mental disorder.

We assume the treatment assignment is ignorable conditional on all the pretreatment variables

#### The Objective

We are using a study to compare the quality of services provided by two physician groups for asthma patients in California. Our objective is to find the average treatment (causal) effect of each physician compared to the other. That is if $p_z$ is the fraction of patients that would be satisfied with the service of $z$ if all patients were treated by the same, then we want to find $p_1 - p_2$.

here is, however, a more interesting insight we can find; We can find which types of people would be more satisified with each of the physician groups. This is a problem known as heterogeneous treatment effect (HTE) estimation. In this project, we will explore how a causal tree-based learning method can find heterogeneity in the treatment effects.


#### The Data

The data is sourced from http://www.biostat.jhsph.edu/~cfrangak/biostat_causal/asthma.txt. We are going to split the data into a training, validation and testing subset such that we can test the model on out-of-sample data.

#### The Model

We are primarily using the work published 2019: "Learning Triggers for Heterogeneous Treatment Effects" by Christopher Tran and Elena Zheleva.
