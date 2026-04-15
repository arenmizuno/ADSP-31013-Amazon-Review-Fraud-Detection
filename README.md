# ADSP 31013 – Big Data and Cloud Computing
## Final Project: Detecting AI-Driven Fraudulent Amazon Reviews Using Similarity Analysis

**University of Chicago**   
**Instructor:** Dmitri Sidorov    
**Term:** Fall 2025 

---

## Overview

This repository contains my final project for *ADSP 31013: Big Data and Cloud Computing*, a course focused on large-scale data processing, distributed computing, and machine learning applications on big data systems.

The course covered key big data technologies and frameworks, including Hadoop and Spark for distributed computation, NoSQL systems, and cloud infrastructure concepts such as virtualization, containers, and orchestration. Emphasis was placed on scalable data processing, similarity search, and real-world applications of big data analytics using Python and PySpark.

---

## Final Project

**Description:**  
This project detects AI-driven fraudulent Amazon reviews using large-scale similarity analysis techniques. The goal is to identify suspicious or duplicated reviews that may indicate automated or coordinated fraud.

The dataset includes over **64 million Amazon reviews** and **4.3 million product metadata records**, processed and cleaned into a large-scale analytical dataset :contentReference[oaicite:0]{index=0}.

---

### Methodology

- Performed **large-scale data preprocessing**:
  - Removed duplicates and invalid records  
  - Filtered incorrect ratings, timestamps, and missing values  
  - Converted timestamps to usable date formats  
  - Reduced dataset to ~63.9M clean reviews  

- Implemented **distributed data processing techniques**:
  - Leveraged big data infrastructure and scalable pipelines  
  - Processed data across large datasets efficiently  

- Conducted **similarity analysis using MinHash + Jaccard distance**:
  - Measured similarity between review titles and full texts  
  - Evaluated duplicate detection at multiple thresholds (0.3, 0.5, 0.7)  
  - Compared duplication patterns across products and time  

- Performed **exploratory analysis**:
  - Review volume trends over time (1998–2023)  
  - Seasonality patterns (holiday spikes, Prime Day effects)  
  - Rating distributions and product-level trends  
  - Reviewer activity and behavior patterns  

---

### Key Findings

- Review volume shows strong growth from 2013–2019, with a spike in 2020 and continued volatility afterward :contentReference[oaicite:1]{index=1}  

- **Title duplication is significantly higher than full-text duplication**, making it a strong signal for fraud detection  

- Duplicate detection increases as similarity thresholds loosen (0.3 → 0.7)  

- **Recent reviews are more unique**, suggesting improved modern fraud detection systems  

- High-review products tend to cluster around **mid-to-high ratings (4.0–4.6)**  

---

### Recommendations

- Use **MinHash + Jaccard similarity pipelines** for scalable fraud detection  

- Focus on **title-based similarity with lower thresholds (≈0.3)** to detect mass-generated reviews  

- Use stricter thresholds for full-text similarity to reduce false positives  

---

### Project Deliverables

- **`notebook_1.ipynb`**  
  → Data cleaning, exploratory data analysis (EDA), and baseline pattern identification across Amazon reviews  

- **`notebook_2.ipynb`**  
  → Text similarity analysis using MinHash LSH to identify duplicate or highly similar review titles and bodies  

- **`notebook_3.ipynb`**  
  → Temporal comparison of similarity-based detection, evaluating effectiveness on older vs. recent reviews  

- **`Final_Presentation.pdf`**  
  → Concise overview of methodology, key findings, and strategic recommendations  

---

## Skills & Concepts Demonstrated

- Big data processing and distributed computing  
- Similarity search: **MinHash, Jaccard distance**  
- Large-scale data cleaning and preprocessing (60M+ records)  
- Exploratory data analysis at scale  
- Fraud detection using pattern recognition  
- Working with cloud-based datasets and pipelines  
- Python and PySpark for big data applications  
- Translating large-scale analytics into actionable insights  

---

## Final Takeaway

This project demonstrates how **scalable similarity analysis techniques** can effectively detect fraudulent behavior in massive datasets.

By leveraging distributed computing and efficient similarity search methods, it is possible to uncover patterns of coordinated or automated activity, providing valuable tools for maintaining data integrity and trust in large online platforms.
