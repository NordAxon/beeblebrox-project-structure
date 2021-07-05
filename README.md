# beeblebrox-project-structure
Default project structure for data science projects


    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    │
    ├── data
    |   |
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   │
    │   └── raw            <- The original, immutable data dump
    |
    ├── notebooks          <- Jupyter notebooks
    |    |
    │    ├── poc           <- Proof of concept notebooks
    |    |
    │    ├── eda           <- Exploratory data analysis
    │    │
    │    ├── modelling     <- Used for training and evaluation documentation
    │    │
    │    └── evaluation    <- Evaluation of model results
    │
    │
    ├── models             <- Storage of model weights, nested by model architecture
    │    |
    │    ├── ARCH_X        <- Directory for architecture X
    |        ├── 001_ARCH_X
    |        │
    |        └── 002_ARCH_X  
    │  
    ├── src                 <- Source code to use in this project.
    |    |
    │    ├── __init__.py    <- Makes src a Python module
    |    |
    │    ├── utils.py       <- General utility functions   
    │    │
    │    ├── preparation    <- Data ingestion and retrieval. Retrieves data and puts in data/raw
    │    │
    │    ├── processing     <- Data transformation and pre-processing. Processes data from data/raw -> data/processed
    │    │
    │    └── modelling      <- Model classes, training and evaluation scripts
    │
    ├── test                <- Code used for testing src/
    │
    │    
    ├── requirements.txt    <- The requirements file for reproducing the analysis environment
    │
    ├── setup.py            <- Makes project pip installable (pip install -e .) so src can be imported

## How to work - phases

#### POC phase

In this phase, you may use some kaggle dataset or a small collected dataset. Focus should be on displaying potential and not building a whole sophisticated system.

Work in notebooks and focus on training a model on your initial dataset and see if there's any potential.

#### Post-POC phase

Now it's time to explore the real data. Start by working in notebooks/eda to really understand the data you're working with. Expand into all the other unused directories as the code you write in the notebooks becomes robust.


## Naming conventions

### Notebooks and executable scripts

To make it easy to run scripts/notebooks in the right order we use a numbering + description convention. 

e.g.

- 01_data_analysis.ipynb

- 03_export_results.py


### Model weight directories

Nested by ARCHITECTURE/NBR_ARCHITECTURE.

e.g.

- models/efficientnet_b0/001_efficientnet_b0

- models/resnet50/001_resnet50


## Requirements and installs

Always try to pin your requirements using pip freeze > requirements.txt

Install the repo 
- in development: pip install -e .
- in production: pip install .

## Optional files and their locations

- Dockfiler: root
- .dockerignore: root
- .env: root

