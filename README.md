# CA_Code: Chained Multi-Label Text Classification

## Overview
This project performs chained multi-label classification on customer interaction data. It predicts three labels for each message: Intent, Tone, and Resolution Type, using a sequence of logistic regression models.

## Folder Structure
- `main.py` - Main script to run the full pipeline (data loading, preprocessing, training, evaluation, and output).
- `preprocessing.py` - Functions for data loading, cleaning, label encoding, and feature extraction.
- `model_chained.py` - Implements the chained model logic.
- `evaluation.py` - Evaluation utilities.
- `models/` - Contains model classes for each label (Intent, Tone, Resolution Type).
- `data/` - Place your input CSV files here (`AppGallery.csv`, `Purchasing.csv`).
- `predictions_output.csv` - Output predictions (created after running `main.py`).
- `evaluation_report.json` - Evaluation metrics (created after running `main.py`).

## Setup
1. **Install dependencies** (recommended: use a virtual environment):
   ```bash
   pip install -r requirements.txt
   ```
2. **Prepare data:**
   - Place your CSV files (`AppGallery.csv`, `Purchasing.csv`) in the `data/` folder.

## Usage
Run the main script:
```bash
python main.py
```

This will:
- Load and preprocess the data
- Train the chained models
- Evaluate predictions
- Save results to `predictions_output.csv` and `evaluation_report.json`

## Output Files
- `predictions_output.csv`: Contains the original message, actual and predicted labels for each test sample.
- `evaluation_report.json`: Contains evaluation metrics for each label and overall chained accuracy.

## Notes
- The code expects the text column to be named `Interaction content` in the CSV files.
- All output files are saved in the same directory as `main.py`.

## Requirements
- Python 3.7+
- See `requirements.txt` for Python package dependencies.

## Contact
For questions or issues, please contact the project maintainer. 
