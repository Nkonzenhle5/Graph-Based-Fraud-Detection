# Graph-Based Fraud Detection

> Traditional machine learning learns from rows.  
> Network science learns from relationships.  
> This project explores whether relationships are the missing ingredient in fraud detection.

---

## Author

**Nkonzenhle Khumalo**

MIS Specialist | Data Analyst | Applied Statistics & Data Science Enthusiast

**Areas of Interest**

- Fraud Analytics
- Network Science
- Machine Learning
- Graph Machine Learning
- Explainable AI
- Applied Statistics

---

## Project Overview

Fraud detection is typically approached as a machine learning classification problem where each transaction is treated as an independent observation.

However, fraudulent activities often involve interconnected entities such as cards, devices, addresses, and accounts that form hidden networks.

This project investigates whether graph-based feature engineering can improve fraud detection performance by incorporating insights from network science into traditional machine learning models. Rather than focusing only on transaction attributes, the project explores whether transaction relationships contain predictive information that traditional tabular approaches may overlook.

---

## Research Question

**Can graph-based features improve fraud detection performance beyond traditional machine learning features?**

---

## Dataset

This project uses the **IEEE-CIS Fraud Detection Dataset**, originally released as part of the IEEE Computational Intelligence Society (CIS) Fraud Detection Competition on Kaggle.

The dataset contains transaction and identity information designed to represent a real-world fraud detection scenario.

### Important Note

The raw IEEE-CIS Fraud Detection dataset is **not included** in this repository due to dataset size constraints and distribution policies.

The dataset can be downloaded directly from Kaggle:

https://www.kaggle.com/competitions/ieee-fraud-detection

Users wishing to reproduce this work should download the dataset separately and run the provided notebook locally.

---

## Methodology

### Baseline Model

The baseline fraud detection model was developed using transaction-level features and trained using XGBoost.

Example feature categories:

- Transaction Amount
- Card Information
- Device Information

---

### Graph Construction

Transaction entities were transformed into network structures.

Relationships were created between entities such as:

- Cards
- Devices
- Addresses

The resulting graphs were analyzed to capture the structure and connectivity of transaction ecosystems.

---

### Graph-Based Features

Several graph-theoretic measures were extracted and incorporated into machine learning models:

- Degree Centrality
- PageRank
- Authority Scores
- Hub Scores

These network-derived features were combined with traditional fraud detection variables and used for model training.

---

## Results

The project compared traditional machine learning models against graph-enhanced models.

### Key Findings

- Graph features do not automatically improve fraud detection.
- Network design plays a critical role in model performance.
- Richer network structures provided stronger predictive signals.
- Relationships between entities may reveal hidden fraud patterns not visible in transaction-level data alone.
- Network science offers a promising complementary perspective to traditional fraud analytics.

---

## Future Research Directions

This project represents an exploratory step toward graph-based fraud detection.

Future work may include:

### Graph Neural Networks (GNNs)

Potential models:

- Graph Convolutional Networks (GCN)
- GraphSAGE
- Graph Attention Networks (GAT)

### Community Detection

Exploring fraud rings using:

- Louvain Communities
- Leiden Algorithm
- Spectral Clustering

### Temporal Network Analysis

Investigating:

- How fraud networks evolve over time
- Emerging fraud communities
- Dynamic graph behavior

### Multiplex Networks

Building multiple relationship layers such as:

- Card ↔ Device
- Card ↔ Address
- Card ↔ Browser
- Card ↔ Email

---

## Questions That Inspired This Work

This project was motivated by several curiosity-driven questions:

- Can a fraudster be identified before committing fraud because of their network position?
- Do fraud networks behave similarly to social networks?
- Are there "super-spreader" devices responsible for a disproportionate amount of fraudulent activity?
- Could fraud detection be viewed as a network epidemiology problem?
- What hidden patterns exist in transaction data that traditional machine learning models cannot see?
- Can graph theory become a core component of future fraud detection systems?

---

## Repository Contents

```text
Graph-Based-Fraud-Detection/
│
├── README.md
├── LICENSE
├── Untitled.ipynb
├── feature_importance.csv
└── model_results.csv
```

---

## Technologies Used

- Python
- Pandas
- NumPy
- NetworkX
- XGBoost
- Scikit-Learn
- Jupyter Notebook

---

## Reproducibility

To reproduce the analysis:

1. Download the IEEE-CIS Fraud Detection dataset from Kaggle.
2. Open the notebook in Jupyter Notebook or JupyterLab.
3. Update local file paths if necessary.
4. Run the notebook sequentially.
5. Review the generated model results and feature importance outputs.

---

## Citation

If this project contributes to your research, report, presentation, or derivative work, please cite:

> Khumalo, N. (2026). *Graph-Based Fraud Detection: Exploring Network Intelligence Beyond Traditional Machine Learning*. GitHub Repository.

---

## Acknowledgements

- IEEE Computational Intelligence Society (IEEE-CIS)
- Kaggle
- Open-source Python ecosystem
- NetworkX
- XGBoost

---

## Final Thought

> Most machine learning models learn from observations.
>
> Graphs learn from relationships.
>
> This project explores whether those relationships can provide a deeper understanding of fraudulent behavior.
