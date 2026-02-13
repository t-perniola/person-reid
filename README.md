## **Project Structure**

The project is organized into the following components:

- `main.ipynb`
Contains the final quantitative and qualitative results of the selected models evaluated on person search metrics (mAP and top-1). This notebook presents the main findings and ablation studies.

- `data_inspection.ipynb`
Provides a preliminary analysis of the PRW dataset, including dataset structure, identity distribution, and inspection of the provided scripts.

- `detection.ipynb`
Reports both quantitative and qualitative results of the detection stage, which constitutes the first step of our two-stage person search pipeline.

- `reid_exploratory_runs.ipynb`
Includes early exploratory experiments conducted to gain preliminary insights into model behavior. These runs were performed before establishing a proper validation protocol. 

- `reid_model_selection.ipynb`
Contains systematic experiments performed on the validation split for hyperparameter tuning and training recipe selection. This notebook documents the model selection process that leads to the final configuration.

**Note 1** Both `reid_exploratory_runs.ipynb` and `reid_model_selection.ipynb` ontain a significantly larger number of experiments compared to those included in `main.ipynb`. These notebooks explore additional configurations such as CosFace loss, Triplet Loss, different learning rate schedulers, and various ablation settings. They document the experimental process that led to the final design choices.

**Note 2** Due to Kaggle’s notebook structure:
- Image visualization requires non-trivial additional code (showing images isn't possible with a simple markdown cell);
- Full modularity is partially limited: importing custom modules across notebooks was not reliably supported in our setup. As a result, several functions are duplicated across notebooks to keep each notebook self-contained and executable.

## **How to run**
The `main.ipynb` notebook is ready to be executed as provided, since the training phase has been disabled and only inference/evaluation is performed.
Before running it, it is recommended to read through the notebook carefully, as it contains detailed comments and qualitative analyses related to selected examples.
The other notebooks are primarily intended for experimentation, visualization, and design exploration. They provide additional insights into architectural choices, loss functions, and training strategies that influenced the final configuration.
The project is designed to run in the [Kaggle](https://www.kaggle.com/) environment. The required datasets must be uploaded beforehand using the provided dataset link.
