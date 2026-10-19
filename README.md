# Speculative Futures: Stress Prediction Using WESAD

## Project Overview

This project investigates stress classification using physiological signals from wearable devices and explores the effects of introducing a hypothetical workplace-surveillance feature for the year 2030.

The project follows an eight-step data science workflow, including topic selection, problem formulation, literature analysis, data preprocessing, feature engineering, speculative feature extraction, model evaluation, and validation.

## Dataset

**Dataset:** WESAD (Wearable Stress and Affect Detection)

**Source:** UCI Machine Learning Repository

**Participants:** 15

**Signal Used:** Chest Electrodermal Activity (EDA)

**Classification Task:** Baseline (0) versus Stress (1), after mapping the original WESAD experimental labels.

The dataset is available at:

https://archive.ics.uci.edu/dataset/465/wesad+wearable+stress+and+affect+detection

The original dataset is not included in this repository.

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Git and GitHub

## Methodology

1. Select and justify a research topic.
2. Define the research problem and measurable objectives.
3. Investigate dataset feasibility and previous research.
4. Process wearable EDA signals using 60-second windows with 30-second steps.
5. Extract statistical features: mean, standard deviation, minimum, maximum, and RMS of first differences.
6. Generate a simulated workplace-surveillance pressure feature for 2030.
7. Train and compare Random Forest classifiers using subject-wise cross-validation.
8. Evaluate reliability using three random seeds and document limitations.

## Experimental Results

The models were evaluated using five-fold subject-wise cross-validation and random seeds 42, 7, and 2026.

| Metric | Baseline Model | Speculative Model |
|---|---:|---:|
| Mean Accuracy | 0.5922 | 0.5751 |
| Mean F1-score | 0.4413 | 0.4097 |
| F1 Standard Deviation | 0.0131 | 0.0090 |

**Mean F1-score difference:** −0.0316

The baseline model performed better than the speculative model in this experiment.

Neither model achieved the predefined F1-score target of 0.85.

## Limitations

- WESAD contains recordings from only 15 participants.
- The measurements were collected in controlled laboratory conditions.
- The model uses a limited selection of EDA features.
- Model performance varies substantially between participants.
- The workplace-surveillance pressure feature is simulated rather than measured.
- The findings do not establish a real-world causal relationship between workplace surveillance and stress.

## How to Run the Project

1. Download the WESAD dataset from the official source.
2. Open `Speculative_Futures_WESAD.ipynb` in Google Colab.
3. Upload the dataset to your own Google Drive.
4. Adjust the dataset paths if your Google Drive folder is different.
5. Connect Google Drive in Colab.
6. Execute the notebook cells in order.
7. Review the generated datasets, charts, and evaluation tables.

The notebook was developed using Google Colab. The Python environment and library versions should be checked before execution.

## Source Code Management

GitHub is used to store the project notebook, document changes, and maintain version history.

The repository includes the notebook, a README, and a `.gitignore` file.

Generated datasets and large raw data files are excluded from GitHub.

## Future Improvements

Future work could examine additional physiological signals, alternative classifiers, more diverse participants, and real-world workplace datasets.

The speculative feature would require empirical validation before being used for practical stress prediction.

## Academic Purpose

This project was developed for a Master's-level Speculative Futures assignment.

The work examines both the technical performance and the assumptions involved in using simulated contextual information for machine learning.
