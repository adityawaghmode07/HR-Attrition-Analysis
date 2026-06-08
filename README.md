# HR-Attrition-Analysis
This project analyzes employee attrition trends using HR data. The dashboard provides insights into employee turnover, job satisfaction, age groups, salary levels, and departmental attrition patterns. The goal is to help organizations understand the key factors influencing employee attrition and improve retention strategies.import pandas as pd
import numpy as np
from pathlib import Path

def generate_sample_hr_data(n_employees=1470):
    """Generate sample HR attrition dataset"""
    
    np.random.seed(42)
    
    data = {
        'EmployeeID': range(1, n_employees + 1),
        'Age': np.random.randint(18, 65, n_employees),
        'Department': np.random.choice(['Sales', 'IT', 'HR', 'R&D'], n_employees),
        'MonthlyIncome': np.random.randint(1000, 15000, n_employees),
        'YearsAtCompany': np.random.randint(0, 40, n_employees),
        'JobSatisfaction': np.random.randint(1, 5, n_employees),
        'WorkLifeBalance': np.random.randint(1, 5, n_employees),
        'EnvironmentSatisfaction': np.random.randint(1, 5, n_employees),
        'JobInvolvement': np.random.randint(1, 4, n_employees),
        'PerformanceRating': np.random.choice([3, 4], n_employees),
        'HourlyRate': np.random.randint(50, 150, n_employees),
        'DistanceFromHome': np.random.randint(1, 30, n_employees),
        'TrainingTimesLastYear': np.random.randint(0, 6, n_employees),
        'PromotionsInLastFiveYears': np.random.randint(0, 3, n_employees),
    }
    
    df = pd.DataFrame(data)
    
    # Create attrition target variable based on factors
    attrition_probability = np.zeros(n_employees)
    
    # Lower satisfaction = higher attrition
    attrition_probability += (5 - df['JobSatisfaction']) * 0.05
    
    # Lower salary = higher attrition
    attrition_probability += (df['MonthlyIncome'].max() - df['MonthlyIncome']) / 1000 * 0.02
    
    # Newer employees more likely to leave
    attrition_probability += np.exp(-df['YearsAtCompany'] / 5) * 0.1
    
    # Young employees more likely to leave
    attrition_probability += (df['Age'] < 30).astype(int) * 0.05
    
    # Add some randomness
    attrition_probability += np.random.normal(0, 0.05, n_employees)
    
    # Convert to binary
    df['Attrition'] = (attrition_probability > 0.3).astype(str).map({True: 'Yes', False: 'No'})
    
    return df

def main():
    """Generate and save sample data"""
    print("Generating sample HR attrition dataset...")
    
    # Create data directory if it doesn't exist
    Path('data').mkdir(exist_ok=True)
    
    # Generate data
    df = generate_sample_hr_data(n_employees=1470)
    
    # Save to CSV
    output_path = 'data/hr_attrition.csv'
    df.to_csv(output_path, index=False)
    
    print(f"✓ Sample data generated and saved to {output_path}")
    print(f"\nDataset Info:")
    print(f"  Total Records: {len(df)}")
    print(f"  Total Features: {len(df.columns)}")
    print(f"  Attrition Rate: {(df['Attrition'] == 'Yes').sum() / len(df) * 100:.2f}%")
    print(f"\nFirst few rows:")
    print(df.head())

if __name__ == "__main__":
    main()

