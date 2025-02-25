# MachineLearning-species-classification-project

## Project Overview

This project is part of the Machine Learning course at The University of Queensland. The goal is to classify species using machine learning algorithms, specifically Principal Component Analysis (PCA) for feature reduction and Random Forest (my choice) for classification. The objective is to improve classification accuracy by selecting the most informative features.

This study includes:

- Feature selection through correlation analysis and PCA.

- Dimensionality reduction using PCA to improve model performance.

- Species classification using Random Forest.

- Performance evaluation with accuracy metrics.

## Project Repository
```
MachineLearning-species-classification-project
│── README.md                  # Project Overview
│── requirements.txt            # List of dependencies
│── data/
│   ├── 83_Loeschcke_et_al_2000_Thorax_&_wing_traits_lab pops.csv  # Dataset
│── images/
│   ├── correlation_map.png      # Correlation heatmap visualization
│   ├── PCA_result.png           # PCA visualization
│   ├── scree_plot.png           # Scree plot for PCA
│── reports/
│   ├── 47801873_Report.pdf      # Final report describing the project
│── notebooks/
│   ├── fly analysis.ipynb       # Jupyter Notebook for full analysis
```

## Setup
1. Clone the repository

`
git clone https://github.com/TsungTseTu122/MachineLearning-species-classification-project.git
`

`
cd MachineLearning-species-classification-project
`

2. Set Up a Virtual Environment (If needed)
For window users:

`
python -m venv venv
venv\Scripts\activate
`

For macOS/Linux users:

`
python3 -m venv venv
source venv/bin/activate
`

3. Install dependencies

`
pip install -r requirements.txt
`

## Dataset overview
The dataset consists of thorax and wing trait measurements from biological samples. The features include:

- Latitude & Longitude: Geographic location of the sample.

- Temperature: Environmental temperature at the time of collection.

- Vial & Replicate: Experimental grouping information.

- Thorax_length: Measurement of the thorax size.

- L2, L3p, L3d, lpd, l3: Wing length measurements from different parts.

- w1, w2, w3: Additional wing-related metrics.

- Wing_loading: A derived trait combining thorax and wing characteristics.

These features were analyzed using correlation heatmaps and PCA to determine their importance in classification.

## How to use
The Jupyter Notebook (`fly_analysis.ipynb`) contains  the complete workflow for analyzing the dataset and training the model. The steps included in the notebook are:
1. Data Preprocessing:

- Loading the dataset and inspecting missing values.

- Converting necessary columns to numerical format.

- Performing correlation analysis to identify highly related features.

2 Feature Selection with PCA:

- Applying Principal Component Analysis (PCA) to reduce dimensionality.

- Determining the optimal number of components using a scree plot.

- Visualizing data distribution in lower-dimensional space.

3. Feature Importance Analysis:

- Extracting and ranking the most influential features in classification.

- Comparing PCA-selected features with the original dataset.

4. Model Training with Random Forest:

- Training a Random Forest classifier on the processed dataset.

- Splitting data into training and testing sets.

- Evaluating model performance using accuracy metrics.

All results are pre-saved, so rerunning is not required.
If you want to modify or extend the analysis, simply open the notebook and adjust the code as needed.

## Key Results

- Feature Selection: PCA was used to reduce dimensionality while preserving important information.

- Visualizations:

  Correlation heatmap to understand feature relationships.
  
  <img src="images/correlation%20map.png" width="650">
  
  Scree plot to determine optimal PCA components.
  
  ![Scree Plot](images/scree%20plot.png)
  
  PCA projection to visualize transformed data.
 
  <img src="images/PCA%20result%20.png" width="650">
  
- Feature Importance Ranking: The notebook provides insights into which features contribute the most to classification accuracy.

- Model Performance: Random Forest achieved a final accuracy of 66.67%, improving from a baseline of 51.63%.

## Future improvement
- Try additional classifiers: Support Vector Machines (SVM) or Neural Networks.

- Hyperparameter tuning: Exploring alternative parameter search strategies beyond GridSearchCV such as Bayesian Optimization or RandomizedSearchCV.

- Explore dataset augmentation: Synthetic data generation to improve classification.
