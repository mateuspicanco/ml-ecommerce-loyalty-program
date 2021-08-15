# Machine Learning E-commerce Loyalty Program

*An Udacity Data Scientist Nanodegree capstone project*

Author: [Mateus Gomes](mailto:mpicanco96@gmail.com)

# Description
This repository contains the code, reports and images for an E-commerce Loyalty Program proof of concept built using Machine Learning techniques. It applies concepts of Anomaly Detection to the context of *Customer Segmentation* using the [UK High-value Customers dataset](https://www.kaggle.com/vik2012kvs/high-value-customers-identification) on Kaggle.

The project structure can be defined as:

1. `configs/`: the configuration files used in the project, such as requirements.txt and anaconda environment files;
2. `data/`: the directory contained both raw and processed data produced from the jupyter notebooks;
3. `models/`: any trained models produced during the project;
4. `reports/`: images, markdown files and PDFs for the reports written for this capstone project;
5. `notebooks/`: contains the data processing, EDA and modeling processes documented as jupyter notebooks.

Note: since plotly graphs don't render nicely in github repositories and require some configuration to show up pre-rendered, I generated html copies of the notebooks as well. They can be found in the `reports/` folder.

The final report (which is also a blog post) can be found [here](https://mateuspicanco.medium.com/building-a-ml-based-e-commerce-loyalty-program-9848a93d7463).

# Environment Setup
As discussed in the project's report and the individual jupyter notebooks, this project utilizes two distinct environments, one for performing Data Preparation with `Spark` and other containing the usual machine learning libraries.

To run the environment for Data Preparation steps, one can run the following commands:

```bash
# pulls the official image from docker hub
docker pull jupyter/pyspark-notebook

# runs the container and assigns the present working directory for the container to access -- works fine if you run in the root directory of this repository
docker run -it -p 8888:8888 -v $(pwd):/home/jovyan/work/projects/ jupyter/pyspark-notebook
```

To emulate the development environment for the EDA and modeling sections of the project, one can use the following command with the conda environment file provided:

```bash
# creates a conda environment for the
conda env create -f ./configs/development_environment.yml

# activates the environment:
conda activate name_of_the_environment

# run the jupyter notebooks:
jupyter notebook
```

# Technologies used in this project
- *UI and Data Visualization*: `plotly`;
- *Data Processing*: `pandas`, `numpy`, `pyspark`;
- *Exploratory Analysis*: `seaborn`, `scipy`;
- *Machine Learning*: `sklearn`;
- *Interpretability*: `shap`;

# Downloading the Project
The entire folder for this project can be downloaded in [Google Drive Folder](https://drive.google.com/drive/folders/1Wwl-XteeFY3ildzItSKD5BS58W4bcmNm?usp=sharing)
