# Big Data Concepts & Heavy.AI Demonstration

This section explains the core concepts of Big Data and demonstrates how large datasets can be explored using **Heavy.AI** (formerly OmniSci).  
The goal is to show an understanding of the **Four Vs of Big Data** and how modern tools handle high‑volume, high‑velocity information.

---

## 1. The Four Vs of Big Data

### **Volume**
Refers to the massive amount of data generated every second.  
Examples include logs, social media posts, sensor data, and transaction records.

### **Velocity**
Describes the speed at which data is created, transmitted, and processed.  
Real‑time systems like SIEMs rely on high‑velocity data streams.

### **Variety**
Data comes in many forms: structured (SQL tables), semi‑structured (JSON), and unstructured (text, images, logs).

### **Veracity**
Refers to the trustworthiness and quality of the data.  
Analysts must filter noise, remove duplicates, and validate accuracy.

---

## 2. Heavy.AI Demonstration

To explore Big Data concepts in practice, I used Heavy.AI’s public demo environment to search for cybersecurity‑related tweets.

### Search Performed
I searched for tweets containing the keyword:


This returned thousands of results across multiple geographic regions.

---

## 3. Visual Exploration

Heavy.AI automatically plotted the results on an interactive map, allowing visual analysis of:

- Tweet locations  
- Regional activity levels  
- Patterns in cybersecurity discussions  
- High‑density clusters  

### Tweet Map  
![Tweet Map](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/big_data/screenshots/Map%20showing%20the%20locations%20where%20the%20tweets%20were%20posted.png)

---

## 4. Tweet Results Table

The platform also displayed a sortable table of tweets, showing:

- Tweet text  
- Usernames  
- Timestamps  
- Locations  
- Engagement metrics  

### Tweet Results  
![Tweet Results](https://raw.githubusercontent.com/AlAbbas-cloud/sql-and-splunk-analysis/refs/heads/main/big_data/screenshots/Tweets%20results%2C%20including%20Retweets%20numbers%20and%20users%20and%20Relevance%20Tweets.png)

---

## 5. Why This Matters

Understanding Big Data is essential for cybersecurity because:

- SIEMs like Splunk process massive log volumes  
- Threat intelligence feeds are high‑velocity data streams  
- SOC analysts must filter noise from meaningful signals  
- Attack patterns often emerge only at scale  

This section demonstrates the ability to work with large datasets and interpret visual analytics tools.

---
