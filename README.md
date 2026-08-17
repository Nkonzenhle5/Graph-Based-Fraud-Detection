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

## Research Motivation

Fraud rarely occurs in isolation.

Traditional fraud detection models focus on transaction-level information such as amounts, card details, and device information. However, fraudsters often leave traces through hidden relationships among cards, devices, addresses, and other entities.

This project explores whether network science and graph-based feature engineering can uncover fraud patterns that traditional machine learning approaches may miss.

---

## Research Question

Can graph-based features improve fraud detection performance beyond traditional machine learning features?

---

## Methodology

### Baseline Model

Features used:

- Transaction Amount
- Card Information
- Device Information

Algorithm:

- XGBoost

### Graph-Based Models

Transaction entities were transformed into networks.

Graph features extracted include:

- Degree Centrality
- PageRank
- Authority Scores
- Hub Scores

These graph features were incorporated into XGBoost models and compared against baseline performance.

---

## Key Findings

- Graph features do not automatically improve performance.
- Network design significantly affects model performance.
- Richer transaction networks provide additional predictive information.
- Relationships between entities may reveal hidden fraud structures.

---

## Future Research

I would like to explore:

### Graph Neural Networks (GNNs)

Potential models:

- GraphSAGE
- GCN
- GAT

### Community Detection

Potential methods:

- Louvain
- Leiden
- Spectral Clustering

### Temporal Fraud Networks

Questions:

- How do fraud networks evolve over time?
- Can network growth predict future fraud?

### Multiplex Networks

Combining multiple layers such as:

- Card ↔ Device
- Card ↔ Address
- Card ↔ Browser
- Card ↔ Email

---

## Out-of-the-Blue Questions

This project inspired several curiosity-driven questions:

1. Can fraudsters be identified before committing fraud because of their position in a network?

2. Do fraud rings behave similarly to social networks?

3. Are there "super-spreader" devices responsible for large portions of fraud activity?

4. Could fraud detection be treated as a network epidemiology problem?

5. What hidden structures exist in data that traditional machine learning models cannot see?

---

## Technologies

- Python
- Pandas
- NumPy
- NetworkX
- XGBoost
- Scikit-Learn
- Jupyter Notebook

---

## Research Ownership

This repository contains original exploratory work conducted by Nkonzenhle Khumalo.

The research questions, hypotheses, graph construction methods, feature engineering approaches, and analytical framework represent original intellectual work.

If this repository contributes to academic research, publications, commercial applications, or derivative works, appropriate acknowledgment of the original author is expected.

© 2026 Nkonzenhle Khumalo
