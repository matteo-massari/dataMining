# Scalable Retail Data Mining

A **scalable data mining framework for retail transactions** built with **Python, Apache Spark, and PySpark MLlib**.
The goal of this project is to explore **frequent pattern mining and association rule discovery** in a retail environment while comparing **different algorithmic implementations and scalability strategies**.

The repository contains multiple implementations of **Apriori** and **FP-Growth**, along with experiments designed to evaluate their **performance, memory behavior, and distributed execution**.

The project is structured as an **interactive data mining pipeline implemented in Jupyter notebooks**.

---

# What This Project Does

The project focuses on three main tasks:

### 1. Transaction Mining

Retail transactions are transformed into **market baskets** (sets of purchased items per invoice) to enable pattern mining.

### 2. Frequent Itemset Mining

Multiple implementations are provided:

* **Vanilla Apriori (Python)**
* **Memory-optimized Apriori**

  * triangular matrix counting
  * triples hash counting
* **Distributed Apriori using Spark RDD**
* **FP-Growth using Spark MLlib**

These implementations allow direct comparison between:

* classical algorithms
* optimized memory strategies
* distributed computation

### 3. Association Rule Discovery

Frequent itemsets are used to generate **association rules**, evaluated using:

* support
* confidence
* lift

The notebook also explores **temporal rule changes** by analyzing specific time windows.

---

# Repository Structure

```
.
├── README.md
├── data
│   ├── customers.csv
│   ├── invoice_items.csv
│   ├── products.csv
│   └── purchases.csv
├── data_mining.ipynb
├── output
│   ├── easter_rules_summary.csv
│   ├── rules_easter.csv
│   ├── rules_post_easter.csv
│   └── rules_pre_easter.csv
└── requirements.txt

```

The **main logic of the project lives in the notebook**, where the entire pipeline is implemented and tested.

---

# What Is Already Implemented

The current version includes:
* Data loading with **Spark DataFrames**
* Basic **EDA and preprocessing**
* Construction of **transaction baskets**
* **Apriori implementation (Python)**
* **Optimized Apriori**
  * triangular matrix counting
  * triples counting
* **Distributed Apriori with Spark RDD**
* **FP-Growth implementation using Spark MLlib**
* **Algorithm runtime comparison**
* **Dataset scaling experiments**
* **Temporal association rule analysis**

The notebook is structured to allow step-by-step exploration of the algorithms.

---

# Work in Progress
Some components are still being expanded.
Planned improvements include:
* **Streaming pipeline**
  * simulate real-time purchase events
  * incremental model updates
* **Customer segmentation**
  * clustering approaches such as:
    * BIRCH
    * CURE
    * scalable K-Means
* **Bipartite graph for network analysis**
---

# Getting Started
The project uses **Python + Spark**, managed with **uv**.
1) Install uv
```bash
pip install uv
```
2) Create the environment
```bash
uv venv
```
3) Install dependencies
```bash
uv pip install -r requirements.txt
```
4) Make sure Java is installed

