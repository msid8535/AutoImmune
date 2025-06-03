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
 
# Key Findings
- The model successfully identified joint pain as the most important factor influencing Fibromyalgia severity, which is a well-known symptom.
- Interestingly, depression and stress were found to be the second most important factor. This is a less-recognized symptom, highlighting the model's potential to uncover overlooked aspects of a condition.
- This finding suggests that focusing on the mental health aspects of Fibromyalgia could be crucial for treatment and may help reduce hospital visits

# Issues Faced & Solutions
- Problem: The raw CSV data was not structured for direct analysis, with input variables and target outputs in different rows under the same columns. 
    - Solution: We performed a split-filter-join operation. The data was filtered into separate dataframes for input features and target scores, which were then joined on a multi-index of user_id and checkin_date.
- Problem: User-generated data contained numerous typographical errors, abbreviations, and inconsistencies, making standard one-hot encoding unsuitable.
    - Solution: The GapEncoder from the skrub library was used to handle this "dirty" categorical data by encoding it based on latent topics derived from n-gram analysis.

