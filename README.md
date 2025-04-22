#Predict Crop Yield Category
Ankush_202401100400039
🌾 Crop Yield Classification Project
This project uses a Random Forest Classifier to predict crop yield categories — Low, Medium, or High — based on inputs like soil type, rainfall, and seed type.

📁 Dataset
The dataset is assumed to be in a CSV format with the following columns:

soil_type: Numeric or categorical representation of the soil type.

rainfall: Rainfall amount in mm (numeric).

seed_type: Seed variety (categorical, e.g., A, B, C).

yield: Target variable with values such as low, medium, or high.

Make sure your CSV has a column with the name containing "yield" for the target to be auto-detected.

🧠 Machine Learning Algorithm
This project uses the Random Forest Classifier, a powerful and reliable algorithm for classification tasks.

📦 Requirements
Install required packages using:

bash
Copy
Edit
pip install pandas scikit-learn joblib
🛠 How the Code Works
1. load_and_prepare(file_path)
Loads the dataset.

Detects the yield column automatically.

Encodes seed_type and yield using LabelEncoder.

Splits data into X (features) and y (target).

2. train_model(X, y)
Splits the data into training and testing sets (80/20 split).

Trains a RandomForestClassifier on the data.

Prints accuracy score.

3. predict_user_input(model, le_seed, le_yield)
Prompts the user to input:

Soil type (numeric)

Rainfall (in mm)

Seed type (e.g., A, B, C)

Encodes the input, runs prediction, and shows the predicted yield category.

4. main()
Coordinates all functions: data loading, model training, saving model, and user prediction.

💾 Model Saving
The trained model is saved using joblib as:

bash
Copy
Edit
crop_yield_model.joblib
You can reload and reuse it for future predictions without retraining.
