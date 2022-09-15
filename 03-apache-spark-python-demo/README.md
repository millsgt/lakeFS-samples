# Integration of lakeFS with Spark and Python

Start by ⭐️ starring [lakeFS open source](https://go.lakefs.io/oreilly-course) project.

This repository includes Jupyter Notebooks and a sample CSV file to demonstrate integration of lakeFS with Apache Spark, Python and Delta Lake. You can run this demo on your local machine.

## Prerequisites
* Docker installed on your local machine
* lakeFS installed and running on your local machine or on a server or in the cloud. If you don't have lakeFS already running then either use [lakeFS Playground](https://demo.lakefs.io/) which provides lakeFS server on-demand with a single click or refer to [lakeFS Quickstart](https://docs.lakefs.io/quickstart/) doc.

## Setup

1. Start by cloning this repository:

   ```bash
   git clone https://github.com/treeverse/lakeFS-samples && cd lakeFS-samples/03-apache-spark-python-demo
   ```

2. Run following commands to download and run Docker container which includes Python, Spark, Jupyter Notebook, JDK, Hadoop binaries, lakeFS Python client and Airflow (Docker image size is around 4.5GB):

   ```bash
      docker build -t lakefs-spark-python-demo .

      docker run -d -p 8888:8888 -p 4040:4040 -p 8080:8080 --user root -e GRANT_SUDO=yes -v $PWD:/home/jovyan -v $PWD/jupyter_notebook_config.py:/home/jovyan/.jupyter/jupyter_notebook_config.py --name lakefs-spark-python-demo lakefs-spark-python-demo
   ```

3. Open JupyterLab UI [http://127.0.0.1:8888/](http://127.0.0.1:8888/) in your web browser.

## Demo Instructions

Once you have successfully completed setup then open "Spark Demo", "Delta Lake Demo" or "Airflow Demo" notebook from JupyterLab UI and follow the instructions.
