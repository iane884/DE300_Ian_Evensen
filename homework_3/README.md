# Homework 3: MapReduce and Spark

## Contents
- `de300_hw3.ipynb`: source code
- `Dockerfile`: container definition
- `requirements.txt` : Python dependencies
- "DE 300 HW3 GenAIDisclosure.pdf": Generative AI Disclosure

## Local setup (without Docker):
- Install dependencies
   ```
   pip install -r requirements.txt
- Clone this repo and cd into the homework_3 folder
- Launch Jupyter Lab:
  ```
  jupyter lab
- In Jupyter Lab, open de300_hw3.ipynb and run.

## Docker setup:
- Build the image:
  ```
  cd homework_3
  docker build -t de300-hw3 .
- Run the container:
  ```
  docker run --rm -it \
  -p 8888:8888 \
  de300-hw3
- Open in browser:
  ```
  http://localhost:8888/lab
- Run de300_hw3.ipynb from within Jupyter Lab

## Expected Outputs:
tf-idf:
- tf-idf measures for the first 5 documents
SVM:
- Objective value (λ = 0.1)
- First 10 (true_label, predicted_label) pairs


  
