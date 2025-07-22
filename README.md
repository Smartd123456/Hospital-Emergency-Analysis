# Hospital-Emergency-Analysis

## Project overview
This project explores emergency room operations using simulated hospital data to identify key trends and support data-driven healthcare decisions. The dashboard provides real-time insights into patient flow, wait times, admission rates, and medical staff performance.

## Project Goals
- Understand average patient wait times across triage levels.
  
- Identify peak hours of ER usage for staffing optimization
- Analyze common diagnoses and their impact on outcomes
- Monitor doctor workload to ensure balanced patient assignments
- Determine which age groups are more frequently admitted
- Improve hospital response and planning through data storytelling

## Tools used
  - Power BI: for data modeling and visualization
  - Dax: for creating measures
  - Excel: for initial data cleaning
 
## Key Features
-  Dynamic KPI Cards (Total Wait Time, Total Admissions, Diagnosis Count)

-  Triage-level wait time comparison

 - Doctor performance tracking

 - Age group admission trend analysis

 - Patient arrival time trend by hour

 - Outcome distribution chart (Admitted vs Discharge)

### Dax Measures Used
- Average Wait Time = AVERAGE('Hospital Emergency Data '[wait time(mins)]

- Total Admitted = CALCULATE(COUNTROWS('Hospital Emergency Data'), 'Hospital Emergency Data'[Outcome] = "Admitted")

- Diagnosis Count = DISTINCTCOUNT('Hospital Emergency Data'[Diagnosis])

- Total Patient Count = COUNTROWS('Hospital Emergency Data')
  
- Average Wait by Triage = AVERAGEX(VALUES('Hospital Emergency Data'[Triage Level]), CALCULATE(AVERAGE('Hospital Emergency Data'[Wait Time])))
  
## Business Questions
- What is the average patient wait time before being seen by a doctor?

- Which triage level has the longest average wait time?

- What are the most common diagnoses in emergency care?

- Which doctors handle the highest number of patients?

- What percentage of patients are admitted vs discharged?

- Are certain age groups more likely to be admitted?

- What are the busiest hours for patient arrivals?

## Analysis and Insight
#### Average Patient Wait Time:
- The overall average wait time before patients are seen by a doctor is 26.60 minutes.
This suggests the emergency room is functioning fairly well in terms of response time, but there is still room for improvement, especially for lower-priority cases.

#### Wait Time by Triage Level :
- Non-Urgent patients wait the longest at 38.21 minutes, followed by Urgent at 33.16 minutes, while Emergency cases are seen much faster-only 9.71 minutes on average.
#### Most Common Diagnoses:
-  The top diagnosis in the ER is Headache (13 cases), followed by Stroke (11), and Chest Pain (8).
This insight can help hospitals allocate more resources and specialists to address high-frequency conditions.

#### Doctor Workload Distribution:
- Dr. Lee and Dr. Adams saw the highest number of patients (14 and 13 patients, respectively).
Understanding this can help with balancing doctor shifts and preventing burnout.

#### Patient Outcomes:
-  Out of 50 total patients, 16 were admitted (35.56%), while 29 were discharged (64.44%).
This means most Emergency Room (ER) visits result in discharge, which could indicate a high number of mild or non-life-threatening cases.
#### Admissions by Age Group
-  The highest admissions came from patients aged 19-35 and 51-65.
This may suggest these age groups either have more severe symptoms or underlying conditions requiring hospitalization.

#### Busiest Hours for Patient Arrival
-  The highest patient inflow happens between 12 PM and 2 PM, with noticeable peaks around 1 PM and 2 PM.
Hospitals can use this insight to better plan staff availability during midday hours when patient volume is at its highest.

## Conclusion
This emergency room data analysis provides valuable insights into patient flow, diagnosis trends, doctor workload, and admission patterns. The findings show that while emergency cases are handled swiftly, non-urgent patients experience longer wait times. Headaches and strokes are among the most common reasons for ER visits, highlighting areas where medical staff and resources should be prioritized.
Doctor workload varies, with a few doctors handling the majority of patients, suggesting a need for better distribution of duties. Most patients are discharged, but a significant portion, especially among the 19–35 and 51–65 age groups require admission. Peak patient hours between 12 PM and 2 PM indicate the need for increased staffing during those times.
In overall, this analysis can support hospitals in improving emergency room efficiency, optimizing staff schedules, and enhancing patient care delivery.

## Author
Happiness Bassey,
(Data Analyst).
   
