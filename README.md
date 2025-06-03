# Triggers and Symptoms of Chronic Autoimmune diseases

# Background
Overall our goal is to create a more efficient way for patients to record, observe and tackle environmental triggers in order to avoid flares of chronic illnesses. The results from the model would be examined for dependencies and patterns, and thus allow better decision to be made using the saved data and trends.

# Features
- Advanced Feature Extraction: To handle noisy, high-cardinality categorical data from user inputs, we used the GapEncoder from the skrub library. This transforms messy text data into standardized numerical features without extensive manual cleaning.
- Machine Learning Classification: The project employs RandomForestClassifier and HistGradientBoostingClassifier to predict the severity of Fibromyalgia based on the encoded features.
- Data Pre-processing: Implemented steps to clean and restructure a large, messy dataset with nearly 8 million rows. The process involves filtering for the target condition and creating a mapping between daily trackable items and condition severity for each user.

# Version Information
- Language: Python
- Environment: Google Colab
- Core Libraries
    - Pandas
    - Scikit-learn
    - Skrub

