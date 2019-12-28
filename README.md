
# Supervised Learning
## Project: Finding Donors for CharityML

## Introduction
(as provided by Udacity)</br>
CharityML is a fictitious charity organization located in the heart of Silicon Valley that was established to provide
financial support for people eager to learn machine learning. After nearly 32,000 letters were sent to people in the 
community, CharityML determined that every donation they received came from someone that was making more than $50,000 
annually. To expand their potential donor base, CharityML has decided to send letters to residents of California, but to only 
those most likely to donate to the charity. With nearly 15 million working Californians, CharityML has brought you on board to
help build an algorithm to best identify potential donors and reduce overhead cost of sending mail. Your goal will be evaluate
and optimize several different supervised learners to determine which algorithm will provide the highest donation yield while
also reducing the total number of letters being sent.

### Code

Code is provided in the `finding_donors.ipynb` notebook file.</br>
Data visualization code is provided in the `visuals.py` file.</br>
Data is included in the `census.csv` file.</br>

The Project was approached in the following steps:</br>
Each step has been discussed in detail in the `finding_donors.ipynb` jupyter notebook.</br>
- Exploring the Data (_Basic_ Exploratory Data Analyis)
- Preparing the Data 
  - Transforming Skewed Continuous Features (Log transformation)
  - Normalizing Numerical Features (MinMaxScaler)
  - Shuffle and Split Data (train-test split)
- Evaluating Model Performance
  - Set a naive predictor performance benchmark
  - Explained Supervised Learning model with advantages, disadvantages and industry applications .
  - Created a Training and Predicting Pipeline
  - Implemented initial model performance
- Improving Results
  - Chose the Best Model with reasoning
  - Described the Model in Layman's Terms
  - Model Tuning by Hyper-parameter Optimization
  - Evaluated Final Model
- Feature Importance
  - Observed feature relevance
  - Extracted important features
  - Importance of Feature Selection and its effects on the model
### Data

The modified census dataset consists of approximately 32,000 data points, with each datapoint having 13 features. This dataset is a modified version of the dataset published in the paper *"Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid",* by Ron Kohavi. You may find this paper [online](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf), with the original dataset hosted on [UCI](https://archive.ics.uci.edu/ml/datasets/Census+Income).

**Features**
- `age`: Age
- `workclass`: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
- `education_level`: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
- `education-num`: Number of educational years completed
- `marital-status`: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
- `occupation`: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
- `relationship`: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
- `race`: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
- `sex`: Sex (Female, Male)
- `capital-gain`: Monetary Capital Gains
- `capital-loss`: Monetary Capital Losses
- `hours-per-week`: Average Hours Per Week Worked
- `native-country`: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)

**Target Variable**
- `income`: Income Class (<=50K, >50K)
