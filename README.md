# Data challenge - DALI application
This project focuses on exploring and analyzing a dataset from a store to predict profits and optimize warehouse locations. The project is split into two main parts:

## Data Preprocessing 
`data_viz.ipynb`
- Data Visualizations: I categorize the dataset into 5 broad categories and explore  each column using visualizations and correlations. The main objective of this section is to understand the data and find patterns that could be useful. 
- Data Imputation: I fill in missing values for each feature based on mode/mean imputation or using an external dataset (https://www.unitedstateszipcodes.org/zip-code-database/). 
- New columns: Additional features such as shipping time, longitude and latitude, are added to the dataset.

## Machine Learning model 
`ml_model.ipynb`
- Feature selection: I use correlation coefficients for numerical data and ANOVA for categorical data. This helped me narrow down the features used in the models.
- PCA: I used PCA to reduce the dimensionality of the selected features to simplify the dataset while retaining important information. 
- Profit prediction: I use logistic regression and random forest to predict profit using PCA features
- Warehouse prediction: Based on the geographic data, I predicts optimum locations for warehouses using K-means. Additionally, I also predict the optimum number of warehouses and locations using cost analysis.  

# Optional challenge - NLP Sentiment Analysis
`nlp_bert.ipynb`
I finetune a BERT model to classify the sentiment of employee reviews of Google and Amazon (as positive/negative). I preprocess the data by storing each review as an element in a list and assigning positive (0) and negative (1) labels to it. 

The data is downsampled and split into training and testing sets (80-20 split). The BERT tokenizer (BertTokenizerFast) is used to tokenize the sentences with truncation and padding. I then use a confusion matrix to evaluate the model's performance on the test set. The top 10 and bottom 10 sentences are identified based on SHAP scores, and the SHAP values for each selected sentence are visualized using plots. 