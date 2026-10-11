# BIT-TRACE — Bitcoin Transaction Anomaly Investigation

BIT-TRACE is an offline-oriented Bitcoin transaction analysis project focused on unsupervised anomaly detection and investigation support. It explores transaction-level behavioural patterns to help identify unusual activity for further analysis.

## Overview

Bitcoin transactions are pseudonymous, and suspicious activity can be difficult to identify using individual transaction records alone. BIT-TRACE applies unsupervised machine learning techniques to rank potentially unusual transactions and generate analysis outputs that support investigation.

## Key Features

- **Unsupervised anomaly detection:** Uses Isolation Forest and Local Outlier Factor (LOF) to identify unusual transaction patterns.
- **Ensemble scoring:** Combines anomaly scores from multiple detection methods.
- **Temporal analysis:** Examines anomaly patterns across transaction time steps.
- **Investigation outputs:** Produces anomaly rankings, Top-K results, and transaction-level analysis artifacts.
- **Evaluation and analysis:** Includes scripts and notebooks for exploring model outputs and transaction behaviour.

## Dataset

The project uses the Elliptic++ Bitcoin transaction dataset.

The original dataset files are not included in this repository because of their size. Obtain the dataset from its official source and place the required files in the expected local data directory before running the relevant scripts.

Dataset source: [Elliptic++ research dataset](https://github.com/git-disl/EllipticPlusPlus)

Please review the dataset's own terms and citation requirements before using or redistributing it.

## Technology Stack

- **Language:** Python
- **Machine Learning:** scikit-learn
- **Anomaly Detection:** Isolation Forest, Local Outlier Factor
- **Data Analysis:** Pandas, NumPy
- **Development:** Jupyter Notebook, Git

## Repository Structure

```text
bittrace098/
├── src/
│   └── inspect_txs.ipynb
├── .gitignore
└── README.md
```

Additional scripts, notebooks, and analysis modules may be added as the project evolves.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yashikasharmays1511-prog/bittrace098.git
cd bittrace098
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

Install the dependencies required by the notebook or scripts you intend to run. If a `requirements.txt` file is available, use:

```bash
pip install -r requirements.txt
```

Otherwise, install the verified dependencies individually.

### 4. Prepare the dataset

Download the dataset from its official source and configure the local paths expected by the notebook or scripts.

### 5. Run the analysis

Open the notebook in Jupyter or VS Code and execute its cells after configuring the dataset paths and installing the required dependencies.

## Methodology

The anomaly-detection workflow explores Isolation Forest and Local Outlier Factor. An ensemble can combine their outputs to produce a ranked list of unusual transactions.

Anomaly scores indicate unusual behaviour relative to the data and do **not** independently prove that a transaction is illicit. Results should be interpreted alongside the dataset's limitations and additional investigation evidence.

## Limitations

- Results depend on dataset quality, feature selection, preprocessing, and model configuration.
- Unsupervised anomaly detection can flag legitimate but unusual transactions.
- Dataset labels, where available, should be used carefully for evaluation and not automatically treated as model inputs.
- Reproducing results requires the appropriate dataset, dependencies, and configuration.

## Responsible Use

This project is intended for research and analytical exploration. Its outputs should not be treated as definitive evidence of criminal activity or used as the sole basis for accusations or enforcement decisions.

## Acknowledgements

This project builds on the Elliptic++ research dataset. Please consult the dataset's official repository and associated research publication for citation and licensing information.

