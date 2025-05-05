# Predicting Heart Attacks with Hektor

## **Introduction**
First and foremost, I would like acknowledge that this dataset was collected at Zheen Hospital in Erbil, Iraq, from January to May 2019. It includes medical records of patients with the aim of classifying whether an individual had a heart attack. This dataset can be found [here](https://www.kaggle.com/datasets/fajobgiua/heart-attack-risk-assessment-dataset), on kaggle.

The main point of this analysis is to build a supervised classification machine learning model that can help hospital staff with diagnosis and risk assessment in patients.

#### <u>Numerical Columns:</u> 
- **Age** - Patient’s age in years. Older individuals are generally at higher risk for cardiovascular issues.

- **Gender** - A binary indicator:
    - 1 = Male
    - 0 = Female
    
    Gender is a relevant factor in heart disease, with risk profiles varying by sex and age.

- **Heart rate** - Heartbeats per minute. Abnormal heart rate can indicate cardiac stress or underlying issues.

- **Systolic blood pressure** - Pressure in arteries during heartbeats. High systolic values are a significant risk factor for heart attacks.

- **Diastolic blood pressure** - Pressure in arteries between heartbeats. Elevated diastolic pressure also contributes to cardiovascular risk.

- **Blood sugar** - Blood glucose level (in mg/dL).

- **CK-MB** - Creatine kinase-MB enzyme level, a cardiac biomarker. High levels can indicate heart muscle damage.

- **Troponin** - A protein released into the blood when the heart muscle is damaged. Elevated levels are strongly associated with
heart attacks.

#### <u>Categorical Columns:</u>

- **Result** - Classification of the patient's condition:
    - positive = The patient experienced a heart attack
    - negative = No heart attack detected

- **Risk_Level** - A categorical assessment of the patient's heart attack risk based on clinical indicators. Possible values include:
    - Low
    - Moderate
    - High

- **Recommendation** - Medical or lifestyle advice based on the patient's condition and risk level. Common recommendations include:
    - Immediate medical attention (for high-risk or confirmed cases)
    - Monitor closely and consult doctor (for moderate-risk cases)
    - Maintain healthy lifestyle (for low-risk or preventative cases)

<!-- ## **Data Cleaning**

### Imputation

### Feature Engineering -->

## **Exploratory Data Analysis**
Here is a sample of what the patient data looks like:

|    |   Age |   Gender |   Heart rate |   Systolic blood pressure |   Diastolic blood pressure |   Blood sugar |   CK-MB |   Troponin | Result   | Risk_Level   | Recommendation                     |
|---:|------:|---------:|-------------:|--------------------------:|---------------------------:|--------------:|--------:|-----------:|:---------|:-------------|:-----------------------------------|
|  0 |    63 |        1 |           66 |                       160 |                         83 |           160 |    1.8  |      0.012 | negative | Moderate     | Monitor closely and consult doctor |
|  1 |    20 |        1 |           94 |                        98 |                         46 |           296 |    6.75 |      1.06  | positive | High         | Immediate medical attention        |
|  2 |    56 |        1 |           64 |                       160 |                         77 |           270 |    1.99 |      0.003 | negative | Moderate     | Monitor closely and consult doctor |
|  3 |    66 |        1 |           70 |                       120 |                         55 |           270 |   13.87 |      0.122 | positive | High         | Immediate medical attention        |
|  4 |    54 |        1 |           64 |                       112 |                         65 |           300 |    1.08 |      0.003 | negative | Moderate     | Monitor closely and consult doctor |

The first thing that I wanted to do was look at to see if I could determine any patterns within the dataset by creating some visualizations.

The first thing I did when starting my analysis was breaking the dataset into male and female patients. Aggregating the data showed that in this sample population, the percent of male patients who had a heart attack was 65%, whereas female patients who had a heart attack was 55%:

| Gender   |   Proportion of Positive Heart attack |
|:---------|--------------------------------------:|
| Male     |                                64.72% |
| Female   |                                55.01% |

The first thing I decided to look at was the systolic blood pressure in patients and if there was any correlation to age and/or heart attacks. Below is a visualization depicting the data:

<iframe
src="assets/htmls/male_systolic_blood_pressure.html"
width="800"
height="600"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>Male Age vs Systolic Blood Pressure</em></figcaption>
<br>

At first we may identify the larger density of points between the 45 and 65 years. We do not see much of a correlation between age ***or*** heart attack results when looking at the systolic blood pressure. 

Next was looking at trends in patient's troponin levels. Below is a figure containing troponin levels for males who had a heart attack, and those who did not.

<iframe
src="assets/htmls/male_subplot_fig.html"
width="1100"
height="700"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>Troponin Levels in Male Patients</em></figcaption>
<br>
 
As seen by the visualization, there is no immediate connection between troponin level and age, but there is a clear connection between troponin level and heart attack. This finding reinforces our understanding of troponin as a protein that is released when the heart muscle is damaged. 

Below is a figure for troponine levels in female patients as well, with equal findings.

<iframe
src="assets/htmls/female_subplot_fig.html"
width="1100"
height="700"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>Troponin Levels in Female Patients</em></figcaption>
<br>

I also decided to look at CK-MB levels as well:

<iframe
src="assets/htmls/male_CKMB.html"
width="1100"
height="700"
frameborder="0"
>
</iframe>
<figcaption align="center"><em>CK-MB Levels in Male Patients</em></figcaption>
<br>

This visualization also showcases the pattern of increased CK-MB levels in patients with heart attacks, and lower levels with those who have not had heart attacks.

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