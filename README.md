# Quantium Retail Analytics & Customer Insights Job Simulation

Welcome to my portfolio repository for the **Quantium Data Analytics Job Simulation** completed via Forage. This project replicates real-world data analytics work performed at Quantium, focusing on data preparation, customer segmentation, statistical experimentation, and commercial application.

---

## 📌 Project Overview & Context
Quantium is a leading global data analytics firm specializing in audience generation and retail analytics. In this simulation, I acted as a Data Analyst assigned to the **Chips Category** for a major retail client (Woolworths Group). The objective was to transform raw transaction and customer demographic data into strategic business recommendations regarding customer purchasing behavior and the commercial effectiveness of a new store layout design.

The project is structured into three distinct core tasks:
1. **Task 1: Data Preparation and Customer Analytics** – Understanding customer segments, purchasing drivers, and product preferences.
2. **Task 2: Experimentation and Uplift Testing** – Designing a statistical framework to evaluate the performance of trial store layouts against matched control stores.
3. **Task 3: Analytics & Commercial Application** – Synthesizing insights into a professional client presentation and structured strategic correspondence.

---

## 📂 Repository Structure

To ensure production-grade data engineering and version control standards, the repository is organized as follows:

```microservice
├── data/
│   ├── raw/                           # Raw client data (Git-ignored in production)
│   │   ├── QVI_transaction_data.xlsx  # Raw transaction data
│   │   └── QVI_purchase_behaviour.csv # Customer loyalty profiles
│   └── processed/                     # Cleaned, structured, and feature-engineered datasets
│       └── QVI_consolidated_data.csv  # Unified dataset used for tasks 2 and 3
│
├── notebooks/
│   ├── Quantium_Data_preparation_&_Analysis_Task_1.ipynb  # Data cleaning, EDA, and segmentation
│   └── Quantium_Data_preparation_&_Analysis_Task_2.ipynb  # Metrics scaling, t-tests, and uplift analysis
│
├── documents/
│   ├── Quantium_presentation_Task_3.pdf                   # Final client slide-deck presentation
│   └── Client_Executive_Brief_Mail.docx                   # Formal executive correspondence to Category Manager
│
├── .gitignore                         # Prevents uploading large data files
├── README.md                          # Repository documentation (This file)
└── requirements.txt                   # Project dependencies (pandas, openpyxl, scipy, seaborn, etc.)
```

---

## 🛠️ Detailed Task Breakdown

### Task 1: Data Preparation & Customer Analytics
* **Objective:** Clean raw commercial transaction records and combine them with demographic segments to isolate core purchasing drivers.
* **Key Steps & Methodologies:**
  * **Data Wrangling:** Converted Excel integer dates to standard formats. Screened and purged extreme outliers (e.g., specific transactions involving 200 bags of chips from a single customer profile).
  * **Feature Engineering:** Extracted `pack_size` (grams) and isolated `Brand_Name` from text descriptions (e.g., standardizing *Kettle*, *Smiths*, *Thins*, *Doritos*).
  * **Exploratory Data Analysis (EDA):** Evaluated spending distributions, metrics spikes, and total sales volume.
* **Core Strategic Insights:**
  * A dramatic sales surge occurs throughout December, peaking sharply immediately before Christmas Eve, followed by an operational drop on **December 25** due to nationwide holiday store closures.
  * **Mainstream Young Singles/Couples** represent the highest absolute customer population volume purchasing snacking chips.
  * **Older Families** and **Young Families** dominate the total average transactional unit sizes, purchasing the highest volume of units per basket across all affluence tiers.
  * *Mainstream Young Singles/Couples* are **27% more likely** to purchase a 270g pack of *Twisties Cheese* chips compared to the rest of the market.

### Task 2: Experimentation and Uplift Testing
* **Objective:** Evaluate the commercial effectiveness of a new shop design implemented across three trial stores (**77, 86, and 88**) over a 3-month trial period (Feb 2019 – Apr 2019).
* **Key Steps & Methodologies:**
  * **Control Store Matching:** Developed a python script scoring historical baseline correlation and Euclidean distance across monthly sales and customer transaction volume to establish identical control baselines:
    * **Trial Store 77** $
ightarrow$ Control Store 233
    * **Trial Store 86** $
ightarrow$ Control Store 155
    * **Trial Store 88** $
ightarrow$ Control Store 237
  * **Statistical Uplift Framework:** Scaled control store sales to match trial store performance trends during the pre-trial phase. Conducted independent **Two-Sample t-tests** to evaluate whether the differences during the trial period were statistically significant ($a = 0.05$).
* **Core Strategic Insights:**
  * **Stores 77 and 86** showed remarkable success, yielding statistically significant increases in total gross revenue and individual customer count during the active trial months.
  * **Store 88** demonstrated static or modest performance improvements, suggesting localized macroeconomic variations or differences in foot-traffic elasticity.

### Task 3: Analytics & Commercial Application
* **Objective:** Synthesize technical analytical findings into high-level business recommendations designed for executive retail leaders.
* **Deliverables:**
  * A structured, client-ready 11-page slide deck summarizing methodology, data protection compliance (ISO27001), segment deep-dives, and experimentation outputs.
  * An executive strategic email addressed to the Category Manager detailing critical category recommendations.

---

## 📈 Key Technical Skills Demonstrated
* **Languages & Ecosystem:** Python (Pandas, NumPy, Matplotlib, Seaborn, Scipy.stats).
* **Statistical Methods:** Hypothesis Testing, Two-Sample t-tests, Confidence Intervals, Euclidean Distance Matching, Scaling & Normalization.
* **Domain Competencies:** Retail Analytics, Category Management, A/B Test Experimentation, Consumer Segmentation, Data Anonymization & Governance.

---

## 🚀 How to Run the Analysis
1. Clone the repository: `git clone https://github.com/yourusername/Quantium-Retail-Analytics.git`
2. Install the necessary dependencies: `pip install -r requirements.txt`
3. Execute the Jupyter notebooks sequentially inside the `notebooks/` directory to reproduce the data cleaning and statistical testing visual plots.

---
*Disclaimer: Data and project briefs provided by Quantium Group Pty Ltd as part of the Forage Data Analytics Job Simulation.*
