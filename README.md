# Car-Accident-severity-prediction


## Project Overview
This project aimed to build a machine learning model to predict the severity of road traffic accidents based on environmental conditions and vehicle-specific attributes. The dataset, sourced from the UK’s road safety data, spans five years and includes information about road conditions, weather, and vehicle details. The goal was to determine the seriousness of accidents, classified as fatal, severe, or slight.

## Project Structure
The project is divided into two main Jupyter notebooks:

1. **Data Preparation.ipynb**: Focuses on data cleaning, preprocessing, and exploration.
2. **Feature Engineering & Model Building.ipynb**: Covers feature selection, model training, and evaluation.

## Data Cleaning and Preprocessing
Key preprocessing steps included:

- **Reversing Label Encoding**: Ensured data interpretability by reversing pre-applied label encoding.
- **Column Selection**: Retained only the relevant columns to streamline the dataset.
- **Handling Missing Values**: Managed missing data through deletion or interpolation as appropriate.
- **Removing Bias and Outliers**: Discarded biased categorical columns and removed numerical outliers.
- **Eliminating Irrelevant Data**: Removed rows with non-informative labels such as "unknown."

## Data Exploration and Visualization
Exploratory Data Analysis (EDA) provided insights into the dataset:

- **Distribution Analysis**: Examined the distribution of data for both numeric and categorical columns.
- **Visualization Techniques**:
  - Histograms for visualizing numerical data distributions.
  - Bar charts to show frequency counts for categorical data.
- **Correlation Analysis**: Calculated correlations between features and accident severity to identify key relationships.
- **Feature Understanding**: Recognized that some numerical-seeming features, such as engine capacity, were categorical.

## Modeling Approach
Machine learning models were trained to predict accident severity using various techniques, including:

- **Balanced Random Forest**
- **AdaBoost**
- **XGBoost**

Resampling techniques like SMOTE and RandomOverSampler were applied to address class imbalances.

## Key Insights and Challenges

### Insights
- **Correlation Analysis**: Identified features like light conditions, vehicle maneuver, and age of the vehicle as influential in predicting accident severity.
- **Visualization**: Helped highlight key patterns in accident severity across different conditions.

### Challenges and Learnings
- **Data Complexity**: Managing a large dataset required extensive cleaning and preprocessing.
- **Feature Context**: Understanding the context of each feature was crucial for accurate analysis.
- **Model Performance**: Despite extensive work, the models' performance underscored the need for richer, more robust data.

## Results Summary
- The models showed limited ability to predict minority classes (slight and severe accidents) due to data imbalance.
- The best-performing models were XGBoost and Balanced Random Forest, though the overall F1 macro scores remained low (~0.3 to 0.35).

## Recommendations for Improvement
1. **Advanced Resampling or Ensemble Techniques**: Employing more sophisticated resampling techniques or hybrid ensemble methods may help better address class imbalance.
2. **Feature Engineering**: Further exploration of interaction terms between features or additional contextual factors (e.g., traffic volume or road condition variations) could provide insights into underlying patterns in accident severity.
3. **Alternative Algorithms**: Techniques such as cost-sensitive learning or anomaly detection methods, which could treat minor classes as “rare events,” may offer a different approach to capturing slight and severe accident cases.

## Future Work
To enhance the predictive performance of accident severity models, future efforts could include:

### 1. Incorporating Additional Features
- **Vehicle-Specific Data**: Include data on vehicle speed at the time of impact, airbag deployment, seatbelt usage, and vehicle safety ratings.
- **Driver Information**: Add features like driver age, experience, impairment factors (e.g., alcohol or drug use), and reaction times.
- **Environmental Context**: Gather more granular data on weather conditions, such as visibility distance and real-time precipitation rates.

### 2. Advanced Modeling Techniques
- **Cost-Sensitive Learning**: Implement models that assign higher weights to underrepresented classes to improve predictions for slight and severe accidents.
- **Hybrid Models**: Explore ensemble models that combine different classifiers to capture diverse aspects of the data.
- **Anomaly Detection**: Treat minority classes as rare events and apply anomaly detection techniques to better identify them.

### 3. Data Augmentation
- Use synthetic data generation techniques to create more examples of slight and severe accidents, improving class balance.

### 4. Feature Engineering
- Investigate interaction effects between key features, such as the combined impact of road surface conditions and light conditions.
- Derive new features that capture more complex relationships within the data.

## Usage
1. **Data Preparation**: Run the `Data Preparation.ipynb` notebook to clean and preprocess the data.  
2. **Model Training**: Execute the `Feature Engineering & Model Building.ipynb` notebook to train and evaluate the models.  
3. **Visualization and Analysis**: Explore the visualizations and correlation matrices for insights.  

## Conclusion
This project highlights the importance of thorough data cleaning and preprocessing in machine learning. While the models provided some predictive capability, the results underscore the need for better data quality and more relevant features to improve accuracy. Future efforts should focus on incorporating additional variables such as speed at impact, use of safety features, and detailed driver information to enhance the model's predictive power.

## Acknowledgments
Special thanks to the UK’s road safety data providers for making the dataset available. This project was a valuable exercise in data preprocessing, feature engineering, and the challenges of imbalanced data in machine learning.

## Contact Information
For questions or collaboration opportunities, please contact:

**Name**: [Daniel okeoghene akalamudo]  
**Email**: [Danielakalamudo@gmail.com]  
**GitHub**: [Dankalas]

## Requirements
To reproduce the results, install the following dependencies:

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib seaborn
