Titanic Dataset Analysis
Residency project made by:

Adrian-Nichita Zloteanu
Shafan Nazeer Ahmed
Dataset Summary
The Titanic dataset contains information about passengers aboard the Titanic, including demographic details (age, gender, class), ticket and fare information, and survival status.

Insights
Most passengers were in their 20s–30s, with some infants and older adults present.
Fare values are heavily skewed: most paid under $50, but a few paid over $500.
Survival rates were much higher for women and first-class passengers, which is expected having watched the movie.
Higher fares and younger age groups were associated with increased survival, especially among wealthier passengers.
Data Cleaning
Loaded the dataset and displayed the first few rows to understand its structure.

Performed some clean-ups:

Dropped the 'Cabin' column due to too many missing values.
Filled missing 'Age' values with the median age.
Filled missing 'Embarked' values with the mode.
Removed duplicate rows to ensure data integrity.
Checked for inconsistent or out-of-range values in 'Fare' and 'Age'.
Performed data analysis:

Visualized distributions of 'Age' and 'Fare'
Examined survival rates by gender and passenger class
Explored relationships between age, fare, and survival status
Exploratory Data Analysis Results
Most passengers are in their 20s–30s. There are also some infants and older adults, but nothing too weird or extreme.

Fare is heavily skewed — most people paid under $50, but a few went way over $500.

Survival patterns stood out:

Women had much higher survival rates than men: lines up with “women and children first”.
People in 1st class were way more likely to survive compared to 3rd class.
When looking at age vs fare, survivors leaned toward higher fares, which makes sense given the class difference. There's also a small but clear cluster of younger, wealthier survivors.

Future modeling
This gave us a pretty good idea of what features will matter later. Gender and class are clearly important, so I’ll definitely use them in classification models. Since Fare is very skewed, we might log-transform it to make things more stable. Also, the relationships don’t look very linear, so tree-based models might work better than linear ones.

Since the relationships in the data don’t look very linear and there’s a mix of numeric and categorical features, the bets approach seems to be with tree-based models like Decision Trees or Random Forests. They usually perform better in this kind of setup and don’t need as much preprocessing.

Challenges
Missing Data: Many entries in 'Cabin' were missing, so the column was dropped. Missing 'Age' and 'Embarked' values were filled in using median and mode respectively.
Skewed Distributions: 'Fare' is highly skewed, which may affect modeling. We might do a log transformation in next steps.
Outliers: Outliers in 'Fare' and 'Age' are consistent with real-world expectations and will be retained further.
