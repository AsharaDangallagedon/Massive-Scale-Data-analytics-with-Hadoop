## Massive Scale Data Analytics with Hadoop

This repository contains a Hadoop MapReduce project focused on distributed data processing and large-scale analytics. 

The project explores the use of Hadoop’s core components (HDFS and MapReduce) to process text collections and structured datasets in a distributed environment. It includes custom mapper and reducer implementations, statistical aggregation logic, and financial time-series feature extraction.

The objective is to demonstrate practical understanding of distributed computing, parallel processing, and large-scale data workflows.

---

## Overview

The project consists of four main components:

1. Word occurrence extraction from large text collections  
2. Distributed regular expression search (grep-style processing)  
3. Statistical analysis of structured datasets  
4. Feature extraction from financial time-series data (NASDAQ dataset)

All tasks are implemented using Java-based Hadoop MapReduce jobs and executed in a distributed environment.

---

## 1. Word Count (MapReduce Fundamentals)

A custom MapReduce implementation to:

- Parse web page collections
- Extract text within specific HTML tags
- Compute distributed word frequencies

This component builds foundational understanding of the Map → Shuffle → Reduce workflow and HDFS block processing.

---

## 2. Distributed Regex Search

A distributed grep-style implementation that:

- Searches for patterns using regular expressions
- Processes large text collections in parallel
- Outputs matching lines with associated metadata

This demonstrates how MapReduce can be adapted for search-style workloads across distributed datasets.

---

## 3. Statistical Analysis (Nuclear Decay Dataset)

A MapReduce-based statistical engine that computes:

- Mean
- Median
- Mode
- Minimum
- Maximum
- Frequency distributions

The implementation avoids loading full datasets into memory and instead performs aggregation through reducers.

Outputs were validated externally to confirm correctness.

---

## 4. Financial Data Analysis (NASDAQ Dataset)

Distributed processing of historical stock data to compute:

- Daily price change
- Daily trading range
- Volume rate of change
- Relative Strength Index (RSI)

Results were exported and visualised using Python.

This section demonstrates feature engineering on time-series data within a distributed framework.

---

## Technical Design

The project follows core distributed systems principles:

- Separation of mapping and aggregation logic
- Key-value emission for scalable reduction
- Time-efficient block processing
- Reusable mapper/reducer patterns
- Simple and maintainable class design

Testing was performed via shell scripts to automate Hadoop job execution and validate outputs.

---

## Technologies Used

Java  
Hadoop MapReduce  
HDFS  
Linux shell scripting  
Python (for visualisation)  

---

## Key Concepts Demonstrated

- Distributed batch processing
- Fault-tolerant data storage (HDFS)
- Parallel computation across cluster nodes
- Statistical aggregation using reducers
- Financial feature engineering
- Scalable text processing

---

## Notes

This repository focuses on clarity and correctness of distributed logic rather than cluster-scale performance tuning. 

The implementations are designed to demonstrate understanding of Hadoop’s processing model and its application to real-world analytical tasks.
