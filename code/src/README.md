# Team - Sparkwit
## _Data Reconciliation & Anomaly Detection_


This Streamlit app performs data reconciliation and anomaly detection on historical and real-time data. The app allows users to upload CSV files containing historical and real-time data, processes them based on user input, and provides a reconciled dataset along with anomaly detection results.

## Features

- Upload historical and real-time data.
- Input composite keys, value keys, and date/time fields.
- Detect anomalies using the Isolation Forest algorithm.
- View and download the reconciled dataset.

## Powered by
- Python 3.10+
- Streamlit
- Pandas
- Scikit-learn
- Streamlit - an open-source framework to rapidly build and share beautiful machine learning and data science web apps.


## Steps for local setup in Oracle Linux system:
- Check whether Python3.10+ is installed or else install Python.
- Create/choose directory of choice and create python virtual environment.
- python -m venv venv
- Inside the newly created directory venv, clone the github repository and checkout the main branch
  ```shell
  source bin/activate 
  ```
- Install all the required python modules
  ```shell
  pip install -r requirements.txt 
  ```
- Start streamlit GUI application
  ```shell
  streamlit run app.py --server.port=8085 
  ```
- Test GUI  by hitting the url through browser
  URL : http://localhost:8085

## Usage:

1. Upload Data:
   - Upload the historical data CSV file.
   - Upload the real-time data CSV file.

2. Enter Parameters:
   - Composite Keys: Enter the columns that uniquely identify records (e.g., ID).
   - Value Keys: Enter the columns to monitor for anomalies (e.g., Value).
   - Date/Time Field: Enter the column containing the date or timestamp.

3. Process Data:
   - Click the Process Data button to reconcile the data and detect anomalies.
   - Once processed, download the reconciled dataset by clicking the Download Reconciled Data button.

Output:
The app will generate and display a reconciled dataset with an additional Status and Anomaly Reason column. You can also download this reconciled dataset in CSV format.

Directory Structure:
```
src/
│── app.py                  # Main Streamlit App
│── requirements.txt         # Dependencies
│── models/
│   ├── trend_analyzer.py    # Trend Analysis & Baseline Identification
│   ├── anomaly_detector.py  # AI-based Anomaly Detection
│── utils/
│   ├── data_loader.py       # Load & Preprocess CSVs
│   ├── reconciliation.py    # Reconciliation Logic
│── output/
│   ├── reconciled_data.csv  # Output File
└── README.md                # Documentation
```

License:    
This project is licensed under the MIT License - see the LICENSE file for details.
