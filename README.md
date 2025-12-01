Phishing Websites Dataset – URL-based phishing classification:

🎯 Project Goal

To classify URL data based on patterns and characteristics extracted from the dataset.
To convert each record into TF-IDF text form and train a Naive Bayes classifier.
To predict the URLLength category or value from the given feature set.

📊 Dataset Overview

Dataset loaded from ml model.xlsx.
Contains multiple columns describing URL-related attributes.
Cleaned by removing missing labels and merging rare classes into an “OTHER” group.
Target Label: URLLength
Represents the numeric or categorical length of each URL.
Used as the prediction output of the classification model.

🧱 Features Used

All columns except URLLength are used as features.
Each row is converted into a single text string.
TF-IDF converts this string into numeric vectors for model training.
Common Feature Types in URL Datasets (similar to yours):

URL Components

Protocol (http/https)
Domain, subdomain, path, parameters

URL Attributes

Presence of digits, hyphens, or symbols
Path length, number of directories
Character-level statistics

Security Indicators (if included)

Presence of IP address
Suspicious keywords (e.g., “login”, “verify”)
Random or abnormal string patterns

Metadata Columns

Timestamps
Notes or remarks
Additional descriptive fields

📘 How the Model Uses the Features

All feature values are converted to strings and concatenated into one document.
TF-IDF extracts term importance from the combined text.
Naive Bayes learns correlations between text patterns and URLLength categories.
