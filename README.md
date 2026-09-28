Task 1: Data Preparation — Swynex Technologies
📌 Objective
Prepare a public dataset for data-science work: clean missing values,handle data types, and document all assumptions.

📊 Dataset
Netflix Movies & TV Shows — 8,807 rows × 12 columnsSource: Kaggle (shivamb/netflix-shows)

🧹 Cleaning Steps
Column	Missing	Action	Reason
director	2,634	Filled "Unknown"	Free text, cannot be imputed
cast	718	Filled "Unknown"	Same as above
country	507	Filled "Unknown"	Same as above
date_added	10	Rows dropped	<0.2% of data, negligible loss
rating	4	Filled with mode	Categorical — mode is the safest choice
duration	3	Fixed data error	Duration values misplaced into rating column
💡 Assumptions
Used "Unknown" instead of dropping rows, to preserve maximum data.
Mode used for rating since it is categorical.
Converted date_added to datetime and type/rating to category types.
🛠 Tools
Python · Pandas · NumPy · Google Colab
