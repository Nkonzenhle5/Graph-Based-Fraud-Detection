# Graph-Based Fraud Detection

> Traditional machine learning learns from rows.
>
> Network science learns from relationships.
>
> This project explores whether relationships are the missing ingredient in fraud detection.

---

## Author

**Nkonzenhle Khumalo**

MIS Specialist | Data Analyst | Applied Statistics & Data Science Enthusiast

---

## Project Overview

Fraud detection is traditionally approached as a machine learning classification problem where each transaction is treated as an independent observation. However, fraudulent activities often involve interconnected entities such as cards, devices, addresses, and accounts that create hidden network structures.

This project investigates whether graph-based feature engineering can improve fraud detection performance by incorporating insights from network science into traditional machine learning models.

The goal is to move beyond transaction-level analysis and explore whether transaction relationships contain predictive information that standard tabular approaches may miss.

---

## Research Question

**Can graph-based features improve fraud detection performance beyond traditional machine learning features?**

---

## Dataset

This project uses the **IEEE-CIS Fraud Detection Dataset**, originally released as part of the IEEE Computational Intelligence Society (CIS) Fraud Detection Competition on Kaggle.

Due to dataset size limitations and dataset distribution policies, the raw training and testing datasets are not included in this repository.

Dataset Source:

https://www.kaggle.com/competitions/ieee-fraud-detection

Dataset Characteristics:

- Real-world fraud detection problem
- Highly imbalanced target variable
- Transaction and identity information
- Hundreds of engineered features
- Complex relationships between entities

---

## Methodology

### Baseline Model

The baseline model was developed using traditional transaction-level features and trained using XGBoost.

Features included:

- Transaction Amount
- Card Information
- Device Information

---

### Graph Construction

Transaction entities were transformed into networks where relationships between cards, devices, and other identifiers could be analyzed.

The project explored graph structures connecting entities such as:

- Card IDs
- Device IDs
- Address Information

---

### Graph Features

Several network-based measures were extracted and incorporated into machine learning models:

- Degree Centrality
- PageRank
- Authority Scores
- Hub Scores

These graph-derived features were then combined with traditional fraud detection variables.

---

## Results

The study compared baseline machine learning models against graph-enhanced models.

Key findings include:

- Graph features do not automatically improve model performance.
- Network design plays a critical role in predictive success.
- Richer transaction networks provided more useful information than simpler network representations.
- Relationships between entities can reveal hidden fraud structures that may not be visible in transaction-level features alone.

---

## Future Research Directions

This project is intended as an exploration rather than a final solution.

Future work may include:

### Graph Neural Networks (GNNs)

Potential architectures:

- Graph Convolutional Networks (GCN)
- GraphSAGE
- Graph Attention Networks (GAT)

### Community Detection

Exploring whether fraud rings can be identified through:

- Louvain Communities
- Leiden Clustering
- Spectral Clustering

### Temporal Fraud Networks

Investigating:

- Evolution of fraud networks over time
- Emerging fraud communities
- Dynamic graph structures

### Multiplex Networks

Building multiple transaction relationship layers such as:

- Card ↔ Device
- Card ↔ Address
- Card ↔ Browser
- Card ↔ Email

---

## Questions That Inspired This Work

This project was motivated by several curiosity-driven questions:

- Can a fraudster be identified before committing fraud because of their network position?
- Do fraud networks behave similarly to social networks?
- Are there "super-spreader" devices responsible for a significant portion of fraudulent activity?
- Could fraud detection be approached as a network epidemiology problem?
- What hidden patterns exist in transaction data that traditional machine learning models cannot see?
- Can graph theory eventually become a core component of fraud detection systems?

---

## Repository Structure

```text
Graph-Based-Fraud-Detection/
│
├── README.md
├── LICENSE
├── graph_fraud_detection.ipynb
├── model_results.
