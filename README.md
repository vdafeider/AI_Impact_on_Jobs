# AI INFLUENCE ON JOBS IN 2030 - POWER BI REPORT

![Project Banner](./Images/logo.jpg)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/Python-3.13-blue.svg)](https://www.python.org/downloads/release/python-3130/)

This repository contains a **data analysis project done in Power BI with integration of Python scripts (ML Model)**. It shows the influence of AI on Job Market in 2030. The project uses a **synthetic dataset from Kaggle** to perform descriptive analysis, EDA, ML modeling.

The project demonstrates Power BI’s capabilities for creating interactive, app-like dashboards with modern visual design.

[OPEN DASHBOARD ON MICROSOFT SERVICES](https://app.powerbi.com/view?r=eyJrIjoiMTcxYmYwNDktODg0NC00NzhhLThmOGEtMTZhN2E1ODlmNmNmIiwidCI6IjU5YTZhM2Y5LTMwYWItNDBmZi1hNDZhLWYzZThkZDU4OGZhOSIsImMiOjl9)

*ML Model (and any Python script) doesn't work in public link (Microsoft security limits). To use ML Prediction open report file in Power BI Desktop or in online version after sign in.*

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Dataset](#dataset)
...

---

## Project Overview
AI has become an integral part of modern life, but its impact on jobs market is widely debated. This project detects jobs that are on higher risk of automation, and analyse features (education, years of experience, salary) that may help to save a job.

### Tools used
- **Power Bi** – building report
- **Figma** – prototyping design
- **Pandas**, **NumPy** – data preparation
- **Matplotlib** – visualization
- **Scikit-Learn** – modeling (Random Forest)

**Key components:**
- Dataset: `AI_Impact_On_Jobs_2030_feature_enriched.csv`
- Power BI Report: `AI_impact.pbix`

---

## Objectives
- Analyze the impact of AI and Automation Index on Job Market in 2030
- Find jobs and sectors that are on high risk and those that are safe from risk of automation
- Build Decission Tree that indicates probability frames of risk and its level.
- Train Machine Learning model to predict risk level of automation

---

## Dataset
**File:** AI_Impact_On_Jobs_2030_feature_enriched.csv  - file afted adding Feature Engeneering columns
**Source:** Kaggle  
**Data Source Link:** [open](https://www.kaggle.com/datasets/ayeshaimran123/social-media-and-mental-health-balance/data)  
**Size:** 3000 rows

| Column                     | Description                                                      |
|----------------------------|------------------------------------------------------------------|
| Job_Title                  | The title of the job                                              |
| Average_Salary             | Average annual salary                                              |
| Years_Experience           | Years of experience                                                |
| Education_Level            | Education level                                                    |
| AI_Exposure_Index          | Measure of how much AI impacts or is used in this role            |
| Tech_Growth_Factor         | Indicator of expected technological growth in this job            |
| Automation_Probability_2030| Probability that this job will be automated by 2030               |
| Risk_Category              | Risk classification based on automation or market changes         |
| Skill_1                    | Primary skill                                             |
| Skill_2                    | Secondary skill                                          |
| Skill_3                    | Third skill                                               |
| Skill_4                    | Fourth skill                                               |
| Skill_5                    | Fifth skill                                                |
| Skill_6                    | Sixth skill                                               |
| Skill_7                    | Seventh skill                                              |
| Skill_8                    | Eighth skill                                             |
| Skill_9                    | Ninth skill                                               |
| Skill_10                   | Tenth skill                                               |
| Experience_Band            | Range category of experience             |
| Income_Band                | Range category of income (low, medium, high)                |
| Job_Sector                 | Sector or industry of the job                                      |
| Labour_Group               | Classification of workers       |

---

## App Structure

1. **INSIGHTS** – Desctipti analysis, Exploratory Data Analysis
2. **AUTOMATION TREE** – Decission Tree that indicates probability frames of risk and its level  
3. **ML MODEL** – Machine Learning model to predict risk level of automation

---

## App Interface

![APP INTERFACE](./Images/Interface_1.png)  

![APP INTERFACE](./Images/Interface_2.png)

![APP INTERFACE](./Images/Interface_3.png)

---

## Key Findings
After the correlation study of the visuals attached below, we can observe some relationships between data parameters that may lead to the following conclusions:
![Correlation Heatmap](./Images/correlation_heatmap.png)

- Majority of social media users spent at least 4 - 6 hours daily at screen
- Higher usage of Social media tends to correlate with higher stress levels
- Higher stress levels always lead to lower happiness index
- Low screen time + regular exercise yields the **highest happiness**
- **Instagram** users show **lower average happiness**
- Sleep quality strongly predicts both happiness and stress
- Stress levels are similar across demographics
- To avoid measurable harmful impact of social media on mental health of users the recommended daily screen time should be less than 1 hour combined with detox (exercises and days without SM)
- to see more insights open the [notebook](https://github.com/vdafeider/data_analysis_social_media_vs_mental_health/blob/main/da_social_media_stress.ipynb)  

<img src="./Images/Stress_Level_vs_Daily_Screen_Time_(hrs).png" alt="Stress vs Screen Time" width="600" height="600">
<img src="./Images/platform.png" alt="Stress vs Screen Time" width="1000">
<img src="./Images/complex.png" alt="Complex visualisation" width="700">
<img src="./Images/3d.png" alt="3D visualization" width="700">
* Balance Score is the relation metric of detox index (days without social media, frequent exercises) divided by screen time.

---

## Machine Learning Model
Data Analysis notebook contains entertainment ML Model that predicts happiness and stress levels with probability visualization by users input values (age, sleep quality,  screen time, etc.) 

Below is App interface and prediction example:

<img src="./Images/predictinout.png" alt="Prediction App interface" style="width: 100%">
<p align="center">
  <img src="./Images/predictvis.png" alt="Probability cloud visualisation" width="600">
</p>


Model Performance Metrics
```
MAE: 0.831
RMSE: 1.020
R2: 0.565
```

Those metrics are actually quite solid for a psychological / behavioural regression model — especially considering: 2 targets (multi-output), very noisy human self-reported variables, non-linear interaction effects, small dataset.

---

## Requirements
To use the notebook with analysis

1. Install Python from the official website : https://www.python.org/downloads/

2. Use the included `requirements.txt` for installation:
```
pip install -r requirements.txt
```
Or manually install using terminal:
```
pip install pandas==2.3.3 numpy==2.3.4 matplotlib==3.9.2 seaborn==0.13.2 plotly==6.4.0 scikit-learn==1.7.2 optuna==4.6.0 feature-engine==1.9.3 scipy==1.16.3 jupyter==1.1.1 notebook==7.2.2 gradio==3.43.0 pingouin==0.6.11 networkx==3.1 statsmodels==0.15.2
```
---

## How to Reproduce
### **1. Clone the repository**
```bash
git clone https://github.com/your-username/mental-health-social-media-analysis.git
cd mental-health-social-media-analysis
```

### **2. Set up the environment**
**Linux/macOS:**
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### **3. Run the notebook**
```bash
jupyter notebook
```
Open `da_social_media_stress.ipynb` → **Restart & Run All**.

### **4. Make predictions**
1. Find "Gradio Interface" in notebook and run (shift+ENTER) to use interface of the App on local URL:  http://127.0.0.1:7862

or

2. Manually modify the example user in the notebook (part - "Visualization of prediction with brobability cloud"):
```python
new_user = pd.DataFrame([{
    "Age": 27,
    "Daily_Screen_Time(hrs)": 4.2,
    "Social_Media_Platform": "Instagram",
    "Exercise_Frequency(week)": 4,
    "Days_Without_Social_Media": 1,
    "Sleep_Quality(1-10)": 6
}])
```
Re-run (shift+ENTER) the prediction cells to generate a new probability cloud.

---

## Contributing
Please follow best practices:
- Fork the repository
- Create a feature branch
- Commit with clear messages
- Open a Pull Request

If you plan to contribute regularly, consider adding:
- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`

---

## License
This project is licensed under the **MIT License**.

---

## Credits and Acknowledgements

The content of this project represents the understanding gained from the walkthrough projects provided by **Code Institute**.  

Issues encountered during development were resolved by **leveraging official documentation, community forums, and best practices** from resources including Stack Overflow, Python library documentation, and YouTube tutorials. 

A huge thanks to **John Anih**, who introduced me to this course.

---

## Author
**Volodymyr Babunych**  
📧 vbabunych@gmail.com  
📍 United Kingdom  
🗓️ November 12, 2025
