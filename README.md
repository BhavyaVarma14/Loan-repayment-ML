# Loan-repayment-ML
Introduction: 
This report presents an analysis of loan repayment prediction using machine learning techniques. The dataset used for this analysis contains information about borrowers' credit policies, loan purposes, interest rates, FICO scores, and other relevant attributes.

Dataset Overview:
•	Dataset Shape: 9578 rows × 14 columns

Columns and Meanings:
1.	credit.policy:
o	Indicates whether a customer meets the credit underwriting criteria of the lending institution.
2.	purpose:
o	The purpose of the loan, categorized into various reasons such as debt consolidation, credit card, home improvement, etc.
3.	int.rate:
o	The interest rate on the loan, expressed as a decimal.
4.	installment:
o	The monthly installment owed by the borrower.
5.	log.annual.inc:
o	The natural logarithm of the borrower's annual income.
6.	dti:
o	Debt-to-income ratio, which represents the borrower's total monthly debt payments divided by their gross monthly income.
7.	fico:
o	FICO credit score, a measure of a borrower's creditworthiness based on their credit history.
8.	days.with.cr.line:
o	Number of days the borrower has had a credit line.
9.	revol.bal:
o	Revolving balance, the amount owed by the borrower on their revolving credit accounts.
10.	revol.util:
o	Revolving utilization rate, the proportion of the borrower's available credit that is currently being utilized.
11.	inq.last.6mths:
o	Number of inquiries made by creditors in the last 6 months.
12.	delinq.2yrs:
o	Number of times the borrower has been 30+ days past due on a payment in the last 2 years.
13.	pub.rec:
o	Number of derogatory public records (bankruptcy filings, tax liens, or judgments) on the borrower's credit report.
14.	not.fully.paid:
o	Binary indicator (0 or 1) representing whether the loan was not fully paid.
Data Preprocessing:
•	Checked for null values; no null values found.
•	Encoded the 'purpose' column using Label Encoder to convert categorical labels to numeric form.
Data Visualization:
1.	Histograms:
o	Visualized distribution of FICO scores based on 'credit.policy' and 'not.fully.paid' categories.
2.	Count Plot:
o	Displayed counts of different loan purposes based on the 'not.fully.paid' category.
3.	Joint Plot:
o	Examined relationship between FICO scores and interest rates.
4.	LM Plot:
o	Explored relationship between 'credit.policy', 'not.fully.paid', and FICO scores.
Further Analysis:
1.	Decision Tree:
o	Utilized Decision Tree Classifier with GridSearchCV for hyperparameter tuning.
o	Achieved an accuracy of 84.58% on the test set.
2.	Bagging with Decision Tree:
o	Applied Bagging Classifier with a Decision Tree base estimator.
o	Obtained a mean score of 73.10%, indicating minimal improvement over the Decision Tree.
3.	AdaBoosting with Decision Tree:
o	Employed AdaBoost Classifier with a Decision Tree base estimator.
o	Produced a test accuracy score of 84.59%, comparable to the Decision Tree alone.
4.	Random Forest Classifier:
o	Implemented Random Forest Classifier with 600 estimators.
o	Achieved a test accuracy score of 84.7%, slightly higher than the Decision Tree.
5.	AdaBoosting with Random Forest:
o	Utilized AdaBoost Classifier with a Random Forest base estimator.
o	Attained a test accuracy score of 84.76%, showing similar performance to the Random Forest Classifier alone.
6.	Gradient Boosting:
o	Applied Gradient Boosting Classifier with a learning rate of 0.05.
o	Yielded a test accuracy score of 84.69%, consistent with other ensemble methods.
Conclusion:
•	Throughout various ensemble methods tested, including Bagging, AdaBoosting, Random Forest, and Gradient Boosting, the Random Forest Classifier consistently demonstrated the best performance with an accuracy of 84.7%.
•	Despite minor variations in accuracy scores among different ensemble techniques, the overall predictive performance remained largely similar.
•	Further optimization and exploration of ensemble methods may be warranted to enhance model performance, potentially through feature engineering or alternative algorithms.
