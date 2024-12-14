# Portfolio

## Table of Contents
- [Portfolio](#portfolio)
- [My Learning Journey](#my-learning-journey-data-analytics-projects)
  - [Week-by-Week Learning](#week-by-week-learning-in-class)
- [Descriptive Analysis](#descriptive-analysis)
  - [Project Description](#project-description)
  - [Methodology](#methodology)
    - [Data Collection and Preparation](#1-data-collection-and-preparation)
    - [Data Pipeline Design](#data-pipeline-design)
  - [Insights and Findings](#insights-and-findings)
  - [Recommendations](#recommendations)
  - [Tools and Technologies](#tools-and-technologies)
  - [Deliverables](#deliverables)
- [Data Quality Control](#part-2-data-quality-control)
  - [Project Description](#project-description-1)
  - [Methodology](#methodology-1)
  - [Deliverables](#deliverables-1)
- [Conclusion](#conclusion)

---

## My Learning Journey: Data Analytics Projects

Throughout my 10-week class, I had the opportunity to delve into data analytics, focusing on AWS tools and machine learning services. Below is an overview of my learning, which includes two major projects I worked on, highlighting my experience and insights into AWS cloud solutions and machine learning applications.

---

## Week-by-Week Learning in Class

Over the past 10 weeks, I gained hands-on experience with AWS technologies, including **CloudWatch** and **SageMaker**. The course allowed me to explore a wide range of data analytics techniques, from data ingestion to machine learning workflows.

### Key Topics Covered:
- Data ingestion using AWS S3
- Data profiling with AWS Glue DataBrew
- Data cleaning and transformation
- Data visualization for actionable insights
- Machine learning model development with AWS SageMaker
- Monitoring with AWS CloudWatch

By the end of this course, I was able to build end-to-end data analytics pipelines, leveraging AWS services to clean, analyze, and model data, along with monitoring systems for data quality and performance.

---

# **Descriptive Analysis**

## **Project Description**

**Project Title**: Distribution of Street Usages in Vancouver  
**Objective**: To design and implement a data analytics platform (DAP) that analyzes the distribution of street usage types in Vancouver, focusing on arterial vs. non-arterial streets and determining how many streets fall under each category.  

**Dataset**:  
[View the Dataset](https://opendata.vancouver.ca/explore/dataset/one-way-streets/table/)  
The dataset focuses on one-way street usage in Vancouver. Key features include:  
1. **Street Type**: Categorizes streets as either *Arterial* or *Non-Arterial*.  
   - *Arterial*: Streets primarily designed to handle higher traffic volumes and facilitate intercity transport.  
   - *Non-Arterial*: Streets catering to lower traffic volumes, mainly for local access.  
2. **Geo-location Coordinates**: Useful for GIS integration and mapping visualizations.  
3. **Street Names**: For referencing and validation during analysis.  

---

## **Methodology**

### **1. Data Collection and Preparation**
#### **Data Ingestion**
- Dataset was downloaded from the source website and uploaded to an AWS S3 bucket titled one-way-strt-sprt for proper organization and accessibility.  

![image](https://github.com/user-attachments/assets/bbac43c9-74e6-4cd5-a383-de5ad9043e05)

#### **Data Profiling**
- Conducted data profiling using AWS tools to ensure data quality and integrity.  
- **Key Observations**:  
  - No missing values in the dataset.  
  - Correct data types (e.g., string).  

![image](https://github.com/user-attachments/assets/c823e2ba-1425-489c-93b6-071dd7800a0e)
![image](https://github.com/user-attachments/assets/0767f009-f94f-43be-9417-9a374aa7dd30)

#### **Data Cleaning**
- Cleaned the dataset by:  
  - Removing unnecessary geo-location coordinates and points.  
  - Trimming extra spaces and special characters in relevant columns.  
  - Removing invalid characters and null values using AWS DataBrew.  
- Outputs:  
  - Parquet format for the system folder.  
  - CSV format for the user folder.  

![image](https://github.com/user-attachments/assets/6c9b3dc5-5cf8-4fab-b8f1-329eac00ec4e)
![image](https://github.com/user-attachments/assets/068edfe5-1539-460b-b6ff-e81d04010748)

### **Data Pipeline Design**
- Designed and implemented an ETL pipeline in AWS Glue for further analysis and transformation of the cleaned dataset.  
- **Objective**:  
  - Identify one-way streets in Vancouver.  
  - Categorize streets into arterial and non-arterial types.  

![image](https://github.com/user-attachments/assets/182c3164-75c0-4917-bc0f-135fa449f9b2)

<details>
  <summary>View Project Steps</summary>

- **Step 1**: Data ingestion using AWS S3.
- **Step 2**: Profiling and cleaning the data with AWS Glue DataBrew.
- **Step 3**: ETL pipeline design in AWS Glue.
- **Step 4**: Analysis of one-way streets by category.

</details>

---

## **Insights and Findings**
- The distribution of street usage reveals patterns in how arterial and non-arterial streets are utilized across Vancouver.  
- The processed data provides valuable insights for stratifying street types and enabling more detailed analyses in the future.  

---

## **Recommendations**
- **Urban Planning**: Use the data to optimize city traffic flow, especially on arterial streets.  
- **Further Analysis**: Incorporate additional datasets, such as traffic volume or accident statistics, to enhance insights.  
- **Automated Monitoring**: Develop real-time monitoring systems using similar ETL pipelines for continuous data updates.  

---

## **Tools and Technologies**
- **AWS**: S3, DataBrew, Glue.  
- **Data Formats**: Parquet and CSV.  
- **Visualization Tools**: AWS portal for screenshots and visualization.  

---

## **Deliverables**
- [x] Comprehensive report summarizing the design, methodology, and findings.  
- [x] Screenshots of key steps and outputs.  
- [ ] Presentation materials highlighting project insights and recommendations.  

---

# **Part-2: Data Quality Control**

## **Project Description**  
**Project Title**: Data Quality Control Initiative for One-Way Street Usage in Vancouver  

---

<details>
  <summary>View Methodology</summary>

### **Data Protection**  
- Implemented encryption using **AWS Key Management Service (KMS)** to secure S3 buckets.  
- Enabled **bucket encryption**, **versioning**, and **backup mechanisms**.  

### **Data Observability**  
- Built a **CloudWatch dashboard** to monitor AWS resources.  
- Tracked S3 bucket size, resource utilization, and cost-performance.  

</details>

---

## Conclusion

Through the **Distribution of Street Usages in Vancouver** and **Data Quality Control Initiative** projects, I gained hands-on expertise in designing and implementing data pipelines, ensuring data quality, and utilizing AWS services to deliver actionable insights.  

### Key Takeaways:
- **End-to-End Pipeline Development**: The ability to transform raw data into insightful analytics through AWS services.  
- **Data Quality Control**: Ensuring reliable and accurate datasets for decision-making processes.  
- **Scalable Solutions**: Designing workflows and monitoring systems capable of growing with future needs.  

---
