# Predicting Heart Attacks with Hektor

## **Introduction**
First and foremost, I would like acknowledge that this dataset was collected at Zheen Hospital in Erbil, Iraq, from January to May 2019. It includes medical records of patients with the aim of classifying whether an individual had a heart attack. This dataset can be found [here](https://www.kaggle.com/datasets/fajobgiua/heart-attack-risk-assessment-dataset), on kaggle.

The main point of this analysis is to build a supervised classification machine learning model that can help hospital staff with diagnosis and risk assessment in patients.

#### <u>Numerical Columns:</u> 
- Age - Patient’s age in years. Older individuals are generally at higher risk for cardiovascular issues.

- Gender - A binary indicator:
    - 1 = Male
    - 0 = Female
    
    Gender is a relevant factor in heart disease, with risk profiles varying by sex and age.

- Heart rate - Heartbeats per minute. Abnormal heart rate can indicate cardiac stress or underlying issues.

- Systolic blood pressure - Pressure in arteries during heartbeats. High systolic values are a significant risk factor for heart attacks.

- Diastolic blood pressure - Pressure in arteries between heartbeats. Elevated diastolic pressure also contributes to cardiovascular risk.

- Blood sugar - Blood glucose level (in mg/dL).

- CK-MB - Creatine kinase-MB enzyme level, a cardiac biomarker. High levels can indicate heart muscle damage.

- Troponin - A protein released into the blood when the heart muscle is damaged. Elevated levels are strongly associated with
heart attacks.

#### <u>Categorical Columns:</u>

- Result - Classification of the patient's condition:
    - positive = The patient experienced a heart attack
    - negative = No heart attack detected

- Risk_Level - A categorical assessment of the patient's heart attack risk based on clinical indicators. Possible values include:
    - Low
    - Moderate
    - High

- Recommendation - Medical or lifestyle advice based on the patient's condition and risk level. Common recommendations include:
    - Immediate medical attention (for high-risk or confirmed cases)
    - Monitor closely and consult doctor (for moderate-risk cases)
    - Maintain healthy lifestyle (for low-risk or preventative cases)

<!-- ## **Data Cleaning**

### Imputation

### Feature Engineering -->

## **Exploratory Data Analysis**
The first thing that I wanted to do was look at to see if I could determine any patterns within the dataset by creating some visualizations.

Below is a figure containing troponin levels for males who had a heart attack, and those who did not.

<iframe
src="assets/htmls/male_subplot_fig.html"
width="800"
height="1000"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>Troponin Levels in Male Patients</em></figcaption>
<br>
 
The goal of this visualization was to determine if there was any correlation in troponin levels and age, alongside looking at the average troponin level in male patients with heart attacks, and those without. As seen by the visualization, there is no immediate connection between troponin level and age, but there is a clear connection between troponin level and heart attack. This finding reinforces our understanding of troponin as a protein that is released when the heart muscle is damaged. 

Below is a figure for troponine levels in female patients as well, with equal findings.

<iframe
src="assets/htmls/female_subplot_fig.html"
width="800"
height="1000"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>Troponin Levels in Female Patients</em></figcaption>
<br>


## **Framing a Prediction Problem**

### Classification Ideas

### Final Decision

## **Baseline Model**

#### Categorical

#### Numerical

### Building the Preprocessing Pipeline

### Building the Baseline Model

## **Final Model**

### Building the New Preprocessing Pipeline

### Building the New Preprocessing Pipeline

## **Conclusion**