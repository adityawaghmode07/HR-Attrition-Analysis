# HR-Attrition-Analysis

## Overview

This project analyzes employee attrition trends using HR data to help organizations understand and reduce employee turnover. The dashboard and analysis provide insights into key factors influencing employee attrition, including job satisfaction, age groups, salary levels, and departmental patterns.

**Goal:** Enable organizations to develop data-driven retention strategies by identifying the primary drivers of employee departure.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis & Insights](#analysis--insights)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## Key Features

✅ **Employee Turnover Analysis** - Identify attrition rates and trends  
✅ **Job Satisfaction Insights** - Correlation between satisfaction and attrition  
✅ **Demographic Analysis** - Attrition patterns by age group and salary level  
✅ **Departmental Insights** - Understand which departments have higher turnover  
✅ **Interactive Dashboard** - Visualize trends and patterns  
✅ **Predictive Modeling** - Predict employees at risk of leaving  

---

## Dataset

The project uses HR employee data containing the following features:

- **Employee Demographics:** Age, Department, Job Title, Tenure
- **Compensation:** Salary Level, Monthly Income, Performance Rating
- **Engagement:** Job Satisfaction, Work-Life Balance, Job Involvement
- **Employment Status:** Attrition (Target Variable), Employment Type
- **Additional Metrics:** Years at company, promotions, training hours

**Data Source:** [Specify your data source]  
**Size:** [Number of records and features]  
**Format:** CSV/Excel

---

## Installation

### Prerequisites
- Python 3.8+
- pip or conda package manager

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adityawaghmode07/HR-Attrition-Analysis.git
   cd HR-Attrition-Analysis
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Running the Analysis

1. **Exploratory Data Analysis:**
   ```bash
   python notebooks/01_eda.py
   ```

2. **Build Predictive Model:**
   ```bash
   python scripts/train_model.py
   ```

3. **Generate Dashboard:**
   ```bash
   python scripts/dashboard.py
   ```

4. **View Results:**
   - Open `output/dashboard.html` in your browser
   - Check `output/reports/` for detailed findings

---

## Analysis & Insights

### Key Findings

- **Attrition Rate:** [X%] of employees leave annually
- **Highest Risk Factors:**
  1. Low job satisfaction
  2. High workload/overtime
  3. Limited growth opportunities
  4. Salary dissatisfaction

- **Departmental Trends:** [Department] has highest turnover rate
- **Age Groups:** [Age group] shows highest attrition

### Recommendations

1. Improve job satisfaction through engagement programs
2. Review compensation and benefits alignment
3. Create clear career progression paths
4. Enhance work-life balance initiatives
5. Strengthen manager-employee relationships

---

## Project Structure

```
HR-Attrition-Analysis/
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies
├── data/
│   ├── raw/                  # Original dataset
│   └── processed/            # Cleaned and processed data
├── notebooks/
│   ├── 01_eda.ipynb         # Exploratory data analysis
│   ├── 02_preprocessing.ipynb # Data cleaning and feature engineering
│   └── 03_modeling.ipynb    # Model building and evaluation
├── scripts/
│   ├── train_model.py       # Model training script
│   ├── dashboard.py         # Interactive dashboard
│   └── utils.py             # Helper functions
├── output/
│   ├── dashboard.html       # Interactive visualizations
│   └── reports/             # Analysis reports and findings
└── models/                   # Trained model artifacts
```

---

## Technologies

- **Data Analysis:** pandas, NumPy, Scikit-learn
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Machine Learning:** Scikit-learn, XGBoost, Random Forest
- **Dashboard:** Dash, Streamlit (optional)
- **Statistical Analysis:** SciPy, Statsmodels

---

## Results

### Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | [X%] |
| Precision | [X%] |
| Recall | [X%] |
| F1-Score | [X%] |
| ROC-AUC | [X%] |

### Top Attrition Predictors

1. Job Satisfaction
2. Monthly Income
3. Overtime Hours
4. Years at Company
5. Department

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Contact & Support

**Author:** [Your Name]  
**GitHub:** [adityawaghmode07](https://github.com/adityawaghmode07)  
**Email:** [waghmodeaditya27@gmail.com]

For questions or feedback, please open an issue or contact the project maintainer.

---

## Acknowledgments

- Data source: [Mention data source]
- Inspired by: [Any inspiration or reference projects]
- Thanks to: [Any collaborators or resources]

