# NASA Program Defects:  Classifier Model Comparison

## Problem Statement
When representing real-world scenarios within machine learning models, it is important to know how to compare performance across model architectures. From these comparisons, a data scientist is able to identify the strongest match for problem representation. Additionally, it is important for data scientists to know how fine-tune models within a given architecture both for cross-method comparison and inter-method comparison.

This small project generates five different classifier model architectures that predict the presence of software defects in a given NASA software program. The project generates 10 models for each method using 10-fold cross-validation. The project then captures Area Under Curve scores for cross-method performance comparison. For two of the five models, a given paremeter is fine-tune prior to final cross-validation training and testing.

Technical Note: For the cross-validation process, the parameter “n_jobs” is adjusted so that all but one available system CPU is dedicated to completing the model_selection.cross-validate() call; this is done to improve computing performance.


## Brief Description of the Data

The selected dataset – named “pc4” - is part of the National Aeronautics and Space Administration (NASA) program defect datasets. The set’s data describes earth-orbiting satellite flight software. The datapoints were compiled by Shirabad & Menzies in 2015[1]. For this project, the data is directly imported from OpenML's database located at: https://www.openml.org/search?type=data&status=active&id=1049

The set examples consist of 37 numerical descriptive features and one Boolean target feature which describes whether an example program contained one or more defects. The descriptive features are based on McCabe and Halstead metrics for software complexity. The dataset contains 1458 program instances and no missing values. 
