# Mechanism of Action Prediction Kaggle Competition

## Setup environment
1) Create a virtual environment
2) Activate env and run: pip install -r requirements.txt

## Data Vizualization
Dataset can be visualized by opening and running MoA_visualization.ipynb
Cell 1 to cell 5: Ignore
Cell 6: Load data from csv files
Cell 7: Concat dataframes of features and targets
Cell 8: Investigate existance of NaNs in dataset
Cell 9: Bar plot for CP_TYPE feature (Investigate similarity of categorilas in train and test set)
Cell 10: Same as Cell 9 but for CP_TIME feature
Cell 11: Same but for CP_DOSE feature
Cell 12: Select columns for genes
Cell 13: Print statistics for 9 genes
Cell 14: Plot distribution for 9 randomly picked genes and compare similarity for train and test
Cell 15: Plot distribution of the means of all genes
Cell 16: Plot distributions of 3 genes with highest mean and 3 genes with lowest mean (outliers indicators due to tails which move the mean val)
Cell 17: Features correlation heatmap for genes
Cell 18: Abs corr coef distribution of genes
Cell 19: Scatter plot for genes with highest correlation coef
Cell 20: Scatter plot for genes with lowest corr coef
Cell 21: Bar plot for frequency of true value for first 20 most frequent targets
Cell 22: Pairwise activation heatmap for first 20 most frequent targets

## Data preprocessing and model training
Preprocessing and training can be run with nn_rnn_cnn.ipynb
Cell 1: Import needed libs
Cell 2: Seed everything for reproducible results
Cell 3: Convert all categorical string values to numeric
Cell 4: Scaling function - ignore (MinMaxScaler from scikitlearn is used)
Cell 5: Mean log loss function to evaluate on other data - ignore (not needed)
Cell 6: Function to create and compile the simple feedforward neural net
Cell 7: Function to create and compile the LSTM-baser RNN
Cell 8: Function to create and compile the CNN
Cell 9: Function to adapt input data for the CNN input shape
Cell 10: Function to reduce dimensionality of data by PCA and print cumulative variance
Cell 11: Function to plot the history of metrics (Log loss, F1-Score) of every training process (NN, RNN, CNN)
Cell 12: Load data
Cell 13: Apply map_n_filter (one from Cell 3)
Cell 14 to Cell 16: Ignore
Cell 17: Scale input data in range [0, 1]
Cell 18: Ignore
Cell 19: Get input and output dimension for NNs
Cell 20: Apply PCA transform on input training data
Cell 21: Visualize PCA components
Cell 22 to Cell 24: Create NN, RNN, CNN models
Cell 25: Train simple NN model
Cell 26: Plot history of simple NN
Cell 27: Train RNN model
Cell 28: Plot History of RNN
Cell 29: Train CNN model
Cell 30: Plot history
Cell 31: Ignore
Cell 32: Apply PCA on input test data
Cell 34 to Cell 40: Predict and save submision csv
