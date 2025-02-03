```plaintext
# Automated Flood Prediction ML

This project aims to predict flood occurrences based on various weather parameters. The project includes data fetching, model training, and prediction scripts.

## Project Structure

```
.DS_Store
data/
    FloodPrediction.csv
models/
    flood_prediction_model.pkl
notebooks/
    flood_prediction.ipynb
requirement.txt
scripts/
    data_fetcher.py
    run_pipeline.py
```

- **data/**: Contains the dataset used for training and prediction.
- **models/**: Contains the trained machine learning model.
- **notebooks/**: Contains Jupyter notebooks for data exploration and model training.
- **scripts/**: Contains Python scripts for data fetching and running the prediction pipeline.
- **requirement.txt**: Lists the dependencies required for the project.

## Setup

1. **Clone the repository**:
   ```sh
   git clone https://github.com/anujjainbatu/automated-flood-prediction-ml.git
   ```

2. **Create a virtual environment**:
   ```sh
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**:
   ```sh
   pip install -r requirement.txt
   ```

## Usage

### Data Fetching

To fetch the latest weather data and update the database, run:
```sh
python scripts/data_fetcher.py
```

### Running the Prediction Pipeline

To run the entire prediction pipeline, including data fetching, model prediction, and saving predictions to the database, run:
```sh
python scripts/run_pipeline.py
```

### Automating with Cron Job

To automate the prediction pipeline with a cron job, add the following line to your crontab (e.g., to run the script every day at midnight):
```sh
0 0 * * * /usr/bin/python3 /path/to/your/workspace/scripts/run_pipeline.py
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
