# Hackstory-ctd
Team: Ctrl Alt Del 
Topic: Hate speech recognition model
USP: platform to recognise hate speech and profanity
# Hate Speech Detection Chrome Extension

This project aims to create a Chrome extension for detecting hate speech using a machine learning model. The extension allows users to open a text file or enter text in the provided text box, and it predicts whether the text contains hate speech.

## Prerequisites

To run this Chrome extension, you need to have the following Python libraries installed:

- `nltk`
- `pandas`
- `numpy`
- `scikit-learn`

## Installation

1. Clone the repository or download the source code files.

2. Install the required Python libraries using the following command:
bash
pip install nltk pandas numpy scikit-learn


## Usage

1. Prepare the Data:
   - Ensure you have a dataset (`hate_speech.csv`) with the necessary columns: `tweet` and `class`.
   - Replace the dataset path in the code: `data = pd.read_csv("hate_speech.csv")`.

2. Data Cleaning and Preprocessing:
   - Define the `clean` function to clean the text data.
   - Customize the cleaning steps as per your requirements.
   - Apply the cleaning function to the dataset: `data["tweet"] = data["tweet"].apply(clean)`.

3. Training the Model:
   - Split the dataset into training and testing data using `train_test_split`.
   - Fit the training data into the `CountVectorizer`: `X = cv.fit_transform(x)`.
   - Train the `DecisionTreeClassifier`: `clf.fit(X_train, y_train)`.

4. Chrome Extension:
   - Import the necessary Python libraries: `import tkinter as tk` and `from tkinter import filedialog`.
   - Implement functions for opening and saving text files.
   - Implement the `check_text` function to predict hate speech.
   - Customize the GUI components and appearance as needed.
   - Run the Chrome extension: `window.mainloop()`.

5. Packaging the Extension:
   - Follow the guidelines provided by Google Chrome to package and distribute the extension.

## Contributing

Contributions to this project are welcome. Feel free to open an issue or submit a pull request with any improvements or suggestions.

## License

This project is licensed under the [MIT License](LICENSE).

