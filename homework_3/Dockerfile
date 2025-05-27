# homework_3/Dockerfile

# 1. Use the Jupyter PySpark image
FROM jupyter/pyspark-notebook:latest

# 2. Copy homework code into container’s workdir
USER root
COPY . /home/jovyan/work
USER $NB_UID

# 3. Set working directory
WORKDIR /home/jovyan/work

# 4. Expose Jupyter’s port
EXPOSE 8888

# 6. On container start, launch JupyterLab
CMD ["start.sh", "jupyter", "lab", "--LabApp.token=''", "--LabApp.allow_root=True"]
