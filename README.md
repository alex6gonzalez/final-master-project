# Machine Learning and Causal Inference approaches for systemic multi-disease associations in UK Biobank

Causal inference modeling has captured the attention of many epidemiologists, economics, and machine learning experts in the last few years. The models attempt to discover the causal links between correlated datasets. Rather than just saying “A and B are linked”, these models might allow us to say “A causes B” or the other way around. We propose using traditional machine learning techniques as well as new causal inference modeling approaches to mine UK Biobank data to better infer the causal link between heart and brain diseases. We worked with three datasets derived from the UK Biobank: vascular risk factors, that captures how well the heart works, brain MRI indices, structural imaging data that contains the structure of various brain regions, and heart CMR radiomics, that quantify various changes in heart structures.

Many recent publications have looked at the relationships between single heart and brain diseases. For example, recent work has shown that changes in brain structure correlate with changes in vascular health. Furthermore, past work at the Artificial Intelligence in Medicine Lab at the Universitat de Barcelona has shown that differences in heart CMR radiomics associate with differences in brain imaging. In addition, this same lab has shown that changes in heart CMR radiomics correlate with changes in vascular health. However, no work has shown the relative importance and causal links between these three datasets (heart CMR Radiomics, brain MRI indices and vascular risk factors). Because these connections have been studied independently but not simultaneously, there are potential redundancies in the data. For instance, another group used brain imaging to predict vascular health. However, it’s possible that the brain imaging changes associated with vascular health arise from changes in cardiac imaging. Therefore, brain imaging provides no unique information.

Our aim will be to provide the first combined systemic and multi-disease study of all these variables. We used both traditional machine learning techniques and causal inference approaches. For traditional machine learning approaches we predicted VRFs using brain MRI indices and heart CMR radiomics separately using optimal classifiers. We then combined the two datasets and checked if they performed any better together. If so, we can infer that they provide unique information. After that, we used causal mediation analysis and we assembled graphs of potential relationships between each of the three datasets. We then measured the strength of the connections in these graphs to simultaneously estimate the causal connection between brain diseases, heart diseases, and vascular health.

![Causal connection between brain diseases, heart diseases, and vascular health](https://github.com/alex6gonzalez/final-master-project/blob/master/Figures/final%20graph.png?raw=true)

## 1. Implemented tricks and techniques
> - Factor Analysis as a dimensionality reduction technique.
> - Machine learning techniques to predict vascular health.
> - Feature selection algorithms (SelectKbest).
> - Sampling techniques to reduce imbalanced data such as Random Undersampling, Random Oversampling and SMOTE-TOMEK.
> - Propensity Score Matching Analysis.
> - Mediation Analysis.

## 2. Machine learning algorithms used
> - K-means clustering.
> - Linear regressions.
> - Random Forest.

## 3. Notebooks
[UK Biobank data pre-processing](https://github.com/alex6gonzalez/final-master-project/blob/master/UK%20Biobank%20data%20pre-processing.ipynb)

[K-means Clustering](https://github.com/alex6gonzalez/final-master-project/blob/master/K-means%20Clustering.ipynb)

### 3.1 Factor Analysis
[Factor Analysis Heart CMR Radiomics](https://github.com/alex6gonzalez/final-master-project/blob/master/Factor%20Analysis%20Heart%20CMR%20Radiomics.ipynb)

[Factor Analysis Brain MRI Indices](https://github.com/alex6gonzalez/final-master-project/blob/master/Factor%20Analysis%20Brain%20MRI%20Indices.ipynb)

### 3.2 Propensity Score Matching
[Propensity Score Matching (pscore_match)](https://github.com/alex6gonzalez/final-master-project/blob/master/Propensity%20Score%20Matching%20(pscore_match).ipynb)

[Propensity Score Matching (pymatch)](https://github.com/alex6gonzalez/final-master-project/blob/master/Propensity%20Score%20Matching%20(pymatch).ipynb)

### 3.3 Machine Learning
#### 3.3.1 Predicting gVRF
[Predicting gVRF (FA)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Predicting%20gVRF%20(FA).ipynb)

[Predicting gVRF (Kbest)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Predicting%20gVRF%20(Kbest).ipynb)

#### 3.3.2 Predicting Agrregate Measure of Vascular Risk
##### Undersampling techniques
[Aggregate Measure Undersampling (KBEST)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Undersampling%20(KBEST).ipynb)

[Aggregate Measure Undersampling (FA)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Undersampling%20(FA).ipynb)

##### SMOTE-Tomek techniques
[Aggregate Measure SMOTE-TOMEK (KBEST)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20SMOTE-TOMEK%20(KBEST).ipynb)

[Aggregate Measure SMOTE-TOMEK (FA)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20SMOTE-TOMEK%20(FA).ipynb)

##### Oversampling techniques
[Aggregate Measure Oversampling (KBEST)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Oversampling%20(KBEST).ipynb)

[Aggregate Measure Oversampling (FA)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Oversampling%20(FA).ipynb)

##### Imbalanced data results
[Aggregate Measure Imbalanced (KBEST)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Imbalanced%20(KBEST).ipynb)

[Aggregate Measure Imbalanced (FA)](https://github.com/alex6gonzalez/final-master-project/blob/master/Machine%20Learning/Aggregate%20Measure%20Imbalanced%20(FA).ipynb)

### 3.4 Causal Inference
[Mediation models (Aggregate measure)](https://github.com/alex6gonzalez/final-master-project/blob/master/Causal%20Inference/Mediation%20models%20(Aggregate%20measure)%20(1).ipynb)

[Mediation models (gVRF)](https://github.com/alex6gonzalez/final-master-project/blob/master/Causal%20Inference/Mediation%20models%20(gVRF)%20(1).ipynb)

[Mediation regressions (Brain = M)](https://github.com/alex6gonzalez/final-master-project/blob/master/Causal%20Inference/Mediation%20regressions%20(Brain%20%3D%20M).ipynb)

[Mediation regressions (Heart = M)](https://github.com/alex6gonzalez/final-master-project/blob/master/Causal%20Inference/Mediation%20regressions%20(Heart%20%3D%20M).ipynb)

## 4. Contributions
Contributions are welcome! For bug reports or requests please submit an [submit an issue](https://github.com/alex6gonzalez/final-master-project/issues).

## 5. Contact
Feel free to contact me to discuss any issues, questions or comments.
* GitHub: [alex6gonzalez](https://github.com/alex6gonzalez)
* Linkedin: [Alejandro González Álvarez](https://www.linkedin.com/in/alejandro-gonzalez-alvarez/)

### BibTex reference format for citation for the Code
```
@misc{TFMGonzalez,
title={Machine Learning and Causal Inference approaches for systemic multi-disease associations in UK Biobank},
url={https://github.com/alex6gonzalez/final-master-project},
note={GitHub repository with a collection of Jupyter notebooks intended to study the associations between heart function, heart structure and brain structure},
author={Alejandro Gonzalez},
  year={2020}
}
```
### BibTex reference format for citation for the report of the Master's Thesis

```
@misc{GonzalezMasterThesis,
title={Machine Learning and Causal Inference approaches for systemic multi-disease associations in UK Biobank},
url={},
note={Report of the Master's Thesis: Associations between vascular risk factors, heart CMR radiomics and brain MRI indices in UK Biobank},
author={Alejandro Gonzalez},
  year={2020}
}
```

## License

The content developed by Alejandro Gonzalez is distributed under the following license:

    Copyright 2020 Alejandro Gonzalez

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
