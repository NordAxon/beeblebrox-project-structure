# beeblebrox-project-structure
Default project structure for data science projects


    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    │
    ├── data
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   │
    │   └── raw            <- The original, immutable data dump
    |
    ├── notebooks          <- Jupyter notebooks
    |    |
    │    ├── eda           <- Exploratory data analysis
    │    │
    │    ├── poc           <- Proof of concept notebooks
    │    │
    │    ├── modelling     <- Used for training and evaluation documentation. Train scripts are run here 
    │    │
    │    └── evaluation    <- Evaluation of model results
    │
    │
    ├── models             <- Storage of model weights in separate folders
    │    |
    │    ├── MODEL_X
    │    │
    │    └── MODEL_Y
    │
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



## Naming conventions

### Notebooks and executable scripts

To make it easy to run scripts/notebooks in the right order we use a numbering + description convention. 

e.g.

- 01_data_analysis.ipynb

- 03_export_results.py


### Model weight directories

- TBD


## Requirements and installs

- TBD


## Optional files and their locations

- Dockfiler: root
- .dockerignore: root
- .env: root

