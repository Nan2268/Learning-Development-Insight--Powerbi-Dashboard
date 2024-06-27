
# Learning & Development-Insight-Powerbi-Dashboard




## Problem Statement

The Learning and Development (L&D) Insights Dashboard in Power BI is designed to provide HR professionals, training coordinators, and department heads with comprehensive insights into their organization's training metrics. This dashboard allows users to visualize key performance indicators, track trends, and analyze trainee performance effectively

Steps followed 

#### Step 1: Import and Transform the Data

 
- Load data into Power BI Desktop, dataset is a excel file.
-  Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
-  Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
-  It was observed that in none of the columns contain errors or empty values .
- Establish relationships between different data tables to create a cohesive data model that supports the necessary visualizations.

#### Step 2 : Designing the Header

Design a consistent header for the dashboard that includes the   
    - dashboard title
    - total training hours 
    - training session
    - trinee training hours
    - slicer for indicating monthly analysis

#### Step 3: Top Metrics Insights
 
 - Key Performance Indicators (KPIs):
      - the number of training sessions conducted
      - total training hours
      - average trainer rating. 

Cards and gauges are used to display these metrics prominently at the top of the dashboard for quick reference By using the above factors we predict the top trainee,top trainer and training topic

#### Step 4: Performance Visuals: Trainers and Topics

- Create barchart that display the performance of individual trainers based on training hours and no of trainee.
- Use bar charts  to show the distribution of training topics based on training hours and no of trainee.

#### Step 5: Trend Analysis: Monthly and Departmental

- Monthly Trends: Develop coloumn charts to display the trend of training hours over time.

- Departmental Trends: Create clustered column charts to compare adherence% across different departments.

  adherence% found using dax formula
  Adherence % = sum(tabl_employee[Actual Hrs])/sum(tabl_employee[Target Hrs.])

#### Step 6:  Target Tracking: Trainee Performance

 - Performance Metrics :  using a donout chart for analyzing the trainee  target achievement

   for this a status column is created in employee table and use dax formula to find status of each employee

 status = if([Adherence %] >1,">100%",if([Adherence %]<0.8,"<80%","80-100%"))

#### Step 7: Slicer Integration

 Integrate slicers to enable users to filter the data based on various dimensions such as  departments, training topic,trainee ,Monthly analysis

