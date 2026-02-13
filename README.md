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

**N.B.** Due to Kaggle’s notebook structure:
- Image visualization requires non-trivial additional code (showing images isn't possible with a simple markdown cell);
- Full modularity is partially limited: importing custom modules across notebooks was not reliably supported in our setup. As a result, several functions are duplicated across notebooks to keep each notebook self-contained and executable.
