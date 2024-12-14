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

### **Data Enrichment**  
- Integrated data from **AWS Data Catalog** and **Dynamo DB** for a unified and comprehensive view.  
- Created a database in Dynamo DB to store and manage structured data like key-value pairs. Exported sample items to an **S3 transfer bucket**, enabling easy access and subsequent enrichment steps.  
- Used AWS Glue crawlers to populate the **Data Catalog** and queried the data using **AWS Athena**, ensuring seamless analysis across formats.  

**Screenshots**:  
![image](https://github.com/user-attachments/assets/eacf07ce-e53a-40d8-98df-879882a9ab06)
![image](https://github.com/user-attachments/assets/89d6fd83-59b5-4204-8fcc-63c064d04dd5)
![image](https://github.com/user-attachments/assets/383a21eb-2450-4db2-9db2-153b12c5482b)
![image](https://github.com/user-attachments/assets/ee395900-3144-44c2-b6e1-8c7b8a39caa9)
![image](https://github.com/user-attachments/assets/83ba20dc-e09d-423d-9144-29fc71919ea0)

---

### **Data Protection**  
- Implemented encryption using **AWS Key Management Service (KMS)** to secure S3 buckets.  
- Enabled **bucket encryption**, **versioning**, and **backup mechanisms** to ensure data safety and recovery.  
- Set up **replication** for redundancy and disaster recovery.  

**Screenshots**:  
![image](https://github.com/user-attachments/assets/8d6a0343-f347-4155-a0c2-248478904232)
![image](https://github.com/user-attachments/assets/64ef31b1-3fb2-44b2-ae6b-75f2b3d3d1c8)
![image](https://github.com/user-attachments/assets/f3d58e28-0526-4a3c-92b2-aee49c4a8312)
![image](https://github.com/user-attachments/assets/389e9639-cec0-4682-8fae-20afebce3927)
![image](https://github.com/user-attachments/assets/c770b9bb-bf3d-4bbb-aa36-34aedf66e9bc)

---

### **Data Governance**  
1. **Sensitive Data Detection**: Ensured no sensitive or personally identifiable information (PII) was present in the dataset.  
2. **Data Quality Assurance**: Validated dataset completeness with no missing or null values.  
3. **Data Segregation**: Used conditional routing to segregate data into arterial and non-arterial street types.  
4. **Data Destination**: Stored cleaned and segregated data in destination buckets under a "data quality" folder for further analysis.  

![image](https://github.com/user-attachments/assets/dfc1f559-0eb0-478f-b79c-3a530570783b)

---

### **Data Observability**  
- Built a **Cloud Watch dashboard** to monitor AWS resources and track metrics such as:  
  - S3 bucket size and object count.  
  - Resource utilization for services like EC2.  
  - Cost-performance analysis for effective resource management.  
- Enabled visualization of data and resources to ensure optimal performance and scalability.  

![image](https://github.com/user-attachments/assets/a395edb7-4148-421f-95b2-3e82cead997b)
</details>

---

## Conclusion

Through the **Distribution of Street Usages in Vancouver** and **Data Quality Control Initiative** projects, I gained hands-on expertise in designing and implementing data pipelines, ensuring data quality, and utilizing AWS services to deliver actionable insights.  

### Key Takeaways:
- **End-to-End Pipeline Development**: The ability to transform raw data into insightful analytics through AWS services.  
- **Data Quality Control**: Ensuring reliable and accurate datasets for decision-making processes.  
- **Scalable Solutions**: Designing workflows and monitoring systems capable of growing with future needs.  

---
