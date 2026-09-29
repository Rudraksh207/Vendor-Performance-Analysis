# 🧾 Vendor Invoice Intelligence System

*An intelligent analytics system for vendor invoice analysis, freight cost prediction, risk classification, and procurement insights using Python, SQL, Machine Learning, and Power BI.*

---

## 📌 Table of Contents

* <a href="#overview">Overview</a>
* <a href="#business-problem">Business Problem</a>
* <a href="#dataset">Dataset</a>
* <a href="#tools--technologies">Tools & Technologies</a>
* <a href="#project-structure">Project Structure</a>
* <a href="#data-processing--preparation">Data Processing & Preparation</a>
* <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
* <a href="#machine-learning">Machine Learning</a>
* <a href="#key-insights">Key Insights</a>
* <a href="#dashboard">Dashboard</a>
* <a href="#how-to-run-this-project">How to Run This Project</a>
* <a href="#future-enhancements">Future Enhancements</a>
* <a href="#author--contact">Author & Contact</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

The **Vendor Invoice Intelligence System** is a data-driven analytics and decision-support platform designed to analyze vendor invoices, procurement transactions, freight costs, and inventory-related information.

The system combines **Python, SQL, Machine Learning, Power BI, and Streamlit** to transform raw invoice data into actionable business insights.

It helps organizations understand vendor performance, identify potentially risky invoices, analyze freight expenses, and predict freight costs for better procurement planning.

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Organizations often process large volumes of vendor invoices containing information about products, quantities, prices, freight charges, and vendor details.

Manually analyzing this information can make it difficult to:

* Identify unusual or potentially risky invoices
* Monitor vendor-wise purchasing patterns
* Analyze increasing freight costs
* Estimate future freight expenses
* Compare vendor performance
* Identify costly procurement patterns
* Convert raw invoice data into actionable insights

The project addresses these challenges through automated data processing, analytics, machine learning, and interactive visualization.

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

The project uses structured vendor, invoice, procurement, and inventory-related data.

Key information includes:

* Vendor details
* Invoice information
* Product and inventory details
* Purchase quantities
* Purchase prices
* Freight costs
* Total purchase values
* Historical transaction information

The processed database is maintained using SQLite.

Example database location:

```text
data/inventory.db
```

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

* **Python** – Data processing, analysis, and machine learning
* **Pandas & NumPy** – Data manipulation and numerical analysis
* **Scikit-learn** – Machine learning and model development
* **SQL / SQLite** – Data storage, querying, and aggregation
* **Power BI** – Interactive business intelligence dashboards
* **Streamlit** – Interactive application interface
* **Matplotlib & Seaborn** – Data visualization
* **Jupyter Notebook** – Exploratory analysis and experimentation
* **Git & GitHub** – Version control and project management

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```text
vendor-invoice-intelligence/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── inventory.db
│
├── notebooks/
│   └── exploratory_data_analysis.ipynb
│
├── scripts/
│   ├── data_processing.py
│   ├── database_queries.py
│   └── model_training.py
│
├── models/
│   └── freight_cost_model.pkl
│
├── dashboard/
│   └── vendor_dashboard.pbix
│
├── app/
│   └── streamlit_app.py
│
└── images/
    └── dashboard.png
```

---

<h2><a class="anchor" id="data-processing--preparation"></a>Data Processing & Preparation</h2>

The raw invoice and procurement data is processed before analysis and model development.

Major preprocessing steps include:

* Loading structured invoice and vendor data
* Handling missing and inconsistent values
* Removing duplicate records
* Converting columns into appropriate data types
* Standardizing vendor and product information
* Creating derived financial and procurement metrics
* Aggregating transaction-level information
* Storing processed data in SQLite
* Preparing features for machine learning models

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

EDA is performed to understand vendor purchasing patterns, freight expenses, invoice characteristics, and overall procurement behavior.

The analysis includes:

### Vendor Analysis

* Vendor-wise purchase volume
* Vendor contribution to procurement
* Vendor-wise freight expenditure
* Average purchase value
* Transaction frequency

### Invoice Analysis

* Invoice value distribution
* Purchase quantity patterns
* Freight cost distribution
* Identification of unusual transaction patterns

### Cost Analysis

* Relationship between purchase quantity and freight cost
* Purchase price and total procurement cost
* Vendor-wise cost variations
* Freight cost contribution to overall expenses

### Inventory Analysis

* Product-level purchasing patterns
* Inventory movement
* Purchase quantities
* Potential slow-moving inventory

---

<h2><a class="anchor" id="machine-learning"></a>Machine Learning</h2>

The system incorporates machine learning to support automated decision-making.

### 🚚 Freight Cost Prediction

A regression-based machine learning model is used to estimate freight costs based on relevant procurement and transaction features.

Potential input features include:

* Purchase quantity
* Purchase price
* Vendor information
* Product information
* Transaction characteristics

The predicted freight cost can assist in procurement planning and cost estimation.

### ⚠️ Invoice Risk Classification

A classification model is used to categorize invoices based on their risk characteristics.

The system analyzes relevant invoice and transaction features to identify records that may require additional review.

This provides an additional layer of automated monitoring alongside traditional rule-based analysis.

---

<h2><a class="anchor" id="key-insights"></a>Key Insights</h2>

The system is designed to generate insights such as:

* Vendors contributing significantly to procurement expenditure
* Vendors associated with higher freight costs
* Transactions with unusual cost or quantity patterns
* Relationship between purchase quantity and logistics expenses
* Products or vendors contributing significantly to total procurement costs
* Invoices requiring additional review based on risk classification
* Estimated freight costs for future procurement scenarios

These insights can support procurement teams in vendor evaluation, cost monitoring, and invoice review.

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

The Power BI dashboard provides an interactive view of vendor and invoice performance.

Key dashboard components include:

* Vendor-wise purchase analysis
* Total procurement value
* Freight cost analysis
* Vendor performance comparison
* Invoice risk distribution
* Purchase quantity analysis
* Cost trends
* Interactive filters for vendor, product, and transaction-level analysis

![Vendor Invoice Intelligence Dashboard](images/dashboard.png)

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/vendor-invoice-intelligence.git
cd vendor-invoice-intelligence
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate the environment:

**Windows:**

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Prepare the database

Place the required database file inside:

```text
data/inventory.db
```

Run the required data-processing or database scripts:

```bash
python scripts/data_processing.py
```

### 5. Train the machine learning models

```bash
python scripts/model_training.py
```

### 6. Run the Streamlit application

```bash
streamlit run app/streamlit_app.py
```

### 7. Open the Power BI Dashboard

Open:

```text
dashboard/vendor_dashboard.pbix
```

in Microsoft Power BI Desktop.

---

<h2><a class="anchor" id="future-enhancements"></a>Future Enhancements</h2>

* Real-time invoice ingestion
* Automated invoice anomaly detection
* OCR-based invoice data extraction
* Integration with ERP/procurement systems
* Advanced vendor risk scoring
* Automated email alerts for high-risk invoices
* Improved freight cost forecasting
* Role-based dashboards for procurement and finance teams
* Cloud-based deployment for scalable data processing

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Rudraksh Shukla**
B.Tech – Computer Science & Engineering (Data Science & Artificial Intelligence)

🔗 GitHub: https://github.com/Rudraksh207

---

⭐ If you find this project useful, consider giving the repository a star!
