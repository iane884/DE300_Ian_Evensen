# homework_2/Dockerfile

# 1) Use a slim Python base
FROM python:3.8-slim

# 2) Create and switch to /app
WORKDIR /app

# 3) Copy and install dependencies
COPY requirements.txt .
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      git curl && \
    pip install --no-cache-dir -r requirements.txt && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# 4) Bring in all your HW2 source
COPY . .

# 5) Expose Jupyter’s port
EXPOSE 8888

# 6) Default command: launch Jupyter Lab
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
