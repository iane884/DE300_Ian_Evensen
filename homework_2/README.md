# Homework 2: Two ways with MIMIC-III

## Contents  
- `DE300hw2.ipynb` : source code
- `requirements.txt` : Python dependencies  
- `Dockerfile` : container definition  

## Prerequisites  
- Python 3.8+, Docker 
- AWS profile
- MIMIC-III CSV files

## Local setup  
1. Install dependencies
   ```
   pip install -r requirements.txt
2. Launch jupyter
   ```
   jupyter lab
3. Open jupyter notebook and run all cells

## Expected Outputs:
- Drug usage: one row per ethnicity, top drug_type by total dose (e.g. BASE)
- Procedures by age: top 3 ICD-9 codes per age bracket
- ICU LOS: overall average (~4.5 days), by gender (F > M), by ethnicity (e.g. Black ≈ 7.7 days > White ≈ 4.1 days)

## Docker
  ```
  cd homework_2
  docker build -t hw2 .
  docker run --rm -it -p 8888:8888 -v "$(pwd)":/app hw2
```
In your browser, open the Jupyter Lab URL printed in the logs and run DE300hw2.ipynb.
