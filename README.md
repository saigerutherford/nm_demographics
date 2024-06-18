# nm_demographics

Analysis scripts and figures for our paper (link to be added post peer review) measuring racial bias in normative models of brain structure. 


### To which reference class do you belong? <br> Measuring racial fairness of reference classes with normative modeling.
S. Rutherford, T. Wolfers, C. Fraza, N.G. Harnett, C.F. Beckmann, H.G. Ruhe, A.F. Marquand. (2024)


### Abstract:
Reference classes in healthcare establish healthy norms, such as pediatric growth charts of height and weight, and are used to chart deviations from these norms which represent potential clinical risk. How the demographics of the reference class influence clinical in- terpretation of deviations is unknown. Using normative modeling, a method for building reference classes, we evaluate the fairness (racial bias) in reference models of structural brain images that are widely used in psychiatry and neurology. We test whether including “race” in the model creates fairer models. We predict self-reported race using the deviation scores from three different reference class normative models, to better understand bias in an integrated, multivariate sense. Across all of these tasks, we uncover racial disparities that are not easily addressed with existing data or commonly used modeling techniques. Our work suggests that deviations from the norm could be due to demographic mismatch with the reference class, and assigning clinical meaning to these deviations should be done with caution. Our approach also suggests that acquiring more representative samples is an urgent research priority.

### Figure 1: Overview of analysis workflow.
**A)** Normative models of brain structure were used to generate deviation scores. Three normative models were fit (pre-trained, race not included, and race included) representing two different reference classes and two sets of covariates. **B)** Normative models were estimated for all regions in the Destrieux atlas, a commonly used anatomical brain parcellation. **C)** The effect of self-reported race on the distribution of normative modeling deviation scores was quantified across all three normative models. **D)** Self-reported race was predicted using normative modeling deviation scores as features.

<img src="https://github.com/saigerutherford/nm_demographics/blob/88ff0251f34c0feddd16fcee728052cdc1ecf0f4/figures/MLHC_Figure1.png" width="900" />

### Figure 2: Summary of normative model deviation scores <br> across all three reference classes (pre-trained, race not included, and race included) <br> in HCP and UKB datasets. 
**A)** Average (mean) deviations for all brain regions within all racial groups (columns). **B)** Percentage of extreme deviations (positive and negative) for all brain regions within all racial groups (columns).

<img src="https://github.com/saigerutherford/nm_demographics/blob/88ff0251f34c0feddd16fcee728052cdc1ecf0f4/figures/MLHC_Figure2.png" width="700" />


### Figure 3: Group differences - errors and deviations. 
**A)** Residual errors and **B)** Deviation scores across all three reference classes (pre-trained, race not modeled, and race modeled) in HCP and UKB. The t-statistic is plotted where White individuals are group one, and Asian or Black individuals are group two. Light colors (positive t-stat) represent larger residual errors or deviations in White individuals and dark colors (negative t-stat) represent larger residual errors or deviations in Asian or Black individuals. Brain regions with statistically significant group differences after multiple comparison correction (FDRcorr p < 0.05) are shown.

<img src="https://github.com/saigerutherford/nm_demographics/blob/88ff0251f34c0feddd16fcee728052cdc1ecf0f4/figures/MLHC_Figure3.png" width="700" />

### Figure 4: Prediction of self-reported race.
**A)** In HCP and **B)** in UKB datasets using deviation scores from three different reference class normative models (pre-trained, race not included, and race included) as features. Performance is evaluated with confusion matrices, receiver operator characteristic (ROC) curves, and Area under the ROC curve (AUC). For the confusion matrix interpretation, the diagonal elements show where predicted label == true label, and the off-diagonal elements show mislabeled (predicted label != true label). The confusion matrices were normalized by the true labels to show ratios rather than counts. For interpreting the receiver operator characteristic (ROC) curves, we plot the performance across 5-fold cross validation (lighter colors, thin lines) and the also the mean across all folds (darker colors, thicker lines).

<img src="https://github.com/saigerutherford/nm_demographics/blob/88ff0251f34c0feddd16fcee728052cdc1ecf0f4/figures/MLHC_Figure4.png" width="700" />
