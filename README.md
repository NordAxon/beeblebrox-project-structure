# beeblebrox-project-structure
Default project structure for data science projects

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    │
    ├── data
    |   |
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   │
    │   └── raw            <- The original, immutable data dump.
    |
    ├── notebooks          <- Jupyter notebooks.
    |    |
    │    ├── poc           <- Proof of concept notebooks.
    |    |
    │    ├── eda           <- Exploratory data analysis.
    │    │
    │    ├── modelling     <- Used for modelling exploration and evaluation.
    │    │
    │    └── evaluation    <- Evaluation of model results.
    │
    ├── models             <- Storage of model weights, nested by model architecture.
    │    |
    │    ├── ARCH_X        <- Directory for architecture X.
    |        ├── ARCH_X_001.h5
    |        ├── ARCH_X_001.json
    |        │
    |        └── ARCH_X_002
    │
    ├── src                 <- Source code to use in this project.
    |    |
    │    ├── __init__.py    <- Makes src a Python module.
    |    |
    │    ├── utils.py       <- General utility functions.
    |    |
    │    ├── main.py        <- Main code for running an API/application.
    │    │
    │    ├── app            <- Code used in deployment.
    │    │
    │    ├── preparation    <- Data preparation. Retrieves data and puts in data/raw/, transforms to data/processed/ using src/processing/.
    │    │
    │    ├── processing     <- Data transformation and pre-processing.
    │    │
    │    ├── training       <- Code for training and evaluating models.
    │    │
    │    └── modelling      <- Model classes.
    │
    ├── test                <- Code used for testing src/.
    │
    ├── requirements.txt    <- The requirements file for reproducing the environment.
    │
    ├── setup.py            <- Makes project pip installable so src can be imported.

## How to work - phases

### POC phase

In this phase, you may use some kaggle dataset or a small collected dataset. Focus should be on displaying potential and not building a whole sophisticated system.

### Post-POC phase

Now it's time to explore the real data. Start by working in notebooks/eda to really understand the data you're working with.

When the code you write in the notebooks becomes robust, turn it into functions in src/. If the notebook is still useful for visualization or demonstration purposes, import these functions from src/, otherwise remove the notebook.

Under src/, make sure that all files follow python coding best practices, such as typing, docstrings and naming conventions. All scripts should be used with argparse.

#### Deployment

Deploying a Python API/application should use the file src/main.py. A deployed API/application should ignore everything in this repo except:

- src/app/
- src/processing/
- src/modelling/

and relevant files in

- root/
- models/
- src/

## Naming conventions

### Notebooks and executable scripts

To make it easy to run scripts/notebooks in the right order we use a numbering + description convention. 

e.g.

- 01_data_analysis.ipynb
- 02_model_training.ipynb
- 03_export_results.py

### Model weight directories

Nested by ARCHITECTURE/NBR_ARCHITECTURE.

e.g.

- models/efficientnet_b0/efficientnet_b0_001

- models/resnet50/resnet50_003

## Requirements and installs

Always try to pin your requirements using pip freeze > requirements.txt

Install the repo 
- in development: pip install -e .
- in production: pip install .

## Optional files and their locations

- Dockerfiler: root
- .dockerignore: root
- .env: root
- requirements_dev.txt: root

