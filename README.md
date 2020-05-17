# Emma Jardas, Final Project for BIOF509

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/py4ds/final-project/master?urlpath=lab/tree/final-project.ipynb)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/py4ds/final-project/blob/master/final-project.ipynb)

# Notes
If you want to see the results and process, use the final-project-truedata.ipynb. DO NOT EDIT OR RUN THE NOTEBOOK or else you will get errors because the dataset does not exist. 

If you want to test the code and run the notebook yourself, please use final-porject-fakedata.ipynb.

##Emma Jardas | NIH Department of Bioethics

### **Background**

Clinical practice frequently involves incapacitated patients. Up to:
- **40%** of hospitalized adults
- **70%** of older adults who require treatment decisions
- **95%** of critically ill adults

are unable to make their own treatment decisions due to decisional incapacity (Lepping, Stanly, & Turner, 2015).

**Who should make the decisions on behalf of these patients, and how should they make them?**
- Surrogates (patient-designated or next-of-kin) should make these decisons by trying to guess what treatment their loved one would want.
- This is called the *substituted judgment standard*.
- This methodology aims to promote the autonomy of the patient (Buchanan & Brock, 1989; Beauchamp & Childress, 2013).

**In other words, the primary goal of involving a surrogate in treatment decision-making is to represent the preferences and values of the patient, to help them receive wanted and avoid unwanted treatments.**
- Indeed, 95.5% of patients endorse the goal of receiving wanted and avoiding unwanted treatments (Rid et al., 2015).

**However, there is a huge problem with this approach.** 
- Family member surrogates only accurately identify the patient's treatment preferences about one-half of the time when no treatment clearly promotes the patient’s best clinical interests (Shalowitz, Garrett-Mayer, & Wendler, 2006).

**Furthermore, when 1,169 patients were asked which of 8 goals they prioritized most,**
- only 38.5% chose receiving desired and avoiding undesired treatments
- 20.0% chose minmizing the burden on their family
- 14.6% chose involving their family in the decision
- 20.0% could not choose any one priority.

**This is a serious problem because the current process promotes only the first of the above goals, despite the fact that this goal is not prioritized by a majority of patients. (Indeed, there is no overall majority.) This leaves two questions.**
- Can we promote all 3 goals at once, so that the process serves all patients?
- Can we somehow deduce which process a particular patient prefers?

# **Problem Statement: Can we predict which patients prioritize involving their family over receiving preferred treatments?**

## **Method**

### Population
- 1,169 patients were surveyed from the George Washington University Hospital, across a variety 6 inpatient and outpatient units or clinics

### Outcome Variable
If your family does not know which treatments you would want, would you still want your family to help your doctors make treatment decisions for you?
- Yes, help doctors decide
- No, do not help doctors decide

### Features
- 16 variables including demographics, health information, and relevant experiences 

### Model 
- A decision tree classifier, with hyperparameters tuned via gridsearch
- 10 fold stratified cross validation
- Performance evaluated by ROC curve analyses

## References
I used a number of references to help me build this project. Check them out!

Data Cleaning
- [Print Text in Color](https://stackoverflow.com/questions/8924173/how-do-i-print-bold-text-in-python)
- [Python Data Cleaning Guide](https://towardsdatascience.com/data-cleaning-in-python-the-ultimate-guide-2020-c63b88bf0a0d)
- [Covert Categorical Data to Numerical](https://chrisalbon.com/python/data_wrangling/convert_categorical_to_numeric/)

Data Generation
- [SciKit Make Classification Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_classification.html)

Decision Trees
- [Python Data Science Handbook - Decision Trees](https://jakevdp.github.io/PythonDataScienceHandbook/05.08-random-forests.html)
- [StackAbuse - Decision Trees](https://stackabuse.com/decision-trees-in-python-with-scikit-learn/)
- [TowardsDataScience - Decision Trees](https://towardsdatascience.com/understanding-decision-tree-classification-with-scikit-learn-2ddf272731bd)
- [DataCamp Course - Decision Trees](https://learn.datacamp.com/courses/machine-learning-with-tree-based-models-in-python)

Validation
- [Stratified Cross Validation - Medium](https://medium.com/@haydar_ai/learning-data-science-day-22-cross-validation-and-parameter-tuning-b14bcbc6b012)
-[Cross Validation and Parameter Tuning - Medium](https://medium.com/@haydar_ai/learning-data-science-day-22-cross-validation-and-parameter-tuning-b14bcbc6b012)
-[Cross Validation for Imbalanced Classification - Machine Learning Mastery](https://machinelearningmastery.com/cross-validation-for-imbalanced-classification/)
-[How to Tune a Decision Tree - Towards Data Science](https://towardsdatascience.com/how-to-tune-a-decision-tree-f03721801680)

Evaluating and Visualizing 
- [ROC AUC - Machine Learning Mastery](https://machinelearningmastery.com/roc-curves-and-precision-recall-curves-for-classification-in-python/)
-[Visualizing Decision Trees - Towards Data Science](https://towardsdatascience.com/visualizing-decision-trees-with-python-scikit-learn-graphviz-matplotlib-1c50b4aa68dc)
-[Evaluating Classification - Towards Data Science](https://towardsdatascience.com/evaluating-machine-learning-classification-problems-in-python-5-1-metrics-that-matter-792c6faddf5)