# Credit Risk Modeling

# 1. Objective

Calculate the amount a specific bank would lose by lending to borrowers, as well as the ratio of total funded loans.

# 2. Data

This project is based on a dataset from the Lending Club, consisting loan information from 2007 to 2014 (466k customers * 75 features).

# 3. Methodology

EL = PD * LGD * EAD

* EL (Expected Loss): The amount a lender might lose by lending to a borrower.
* PD (Probability of Default): The borrowers' inability to repay their debt in full or on time (Logistic Regression).
* LGD (Loss Given Default): The proportion of the total exposure that cannot be recovered by the lender once a default has occurred (Logistic Regression + Linear Regression).
* EAD (Exposure at Default): The total value that a lender is exposed to when a borrower defaults (Linear Regression).

# 4. Variable intepretation:

![image](https://user-images.githubusercontent.com/64850893/142494442-c3d93b5a-90d6-4a7b-a187-aaac1975296d.png)

![image](https://user-images.githubusercontent.com/64850893/142494551-9060105e-60a6-46bc-84ab-1ac4f3b8ebcc.png)

# 5. PD Model:

## 5.1 Data Prep and EDA

* Dependent Variable: Good/ Bad (Default) Definition, which means Default and Non-default Accounts.

* Preprocessing Discrete Variables: calculate WOE (Weight of Evidence) and IV (information value), visualizing results, creating dummy variables.

![image](https://user-images.githubusercontent.com/64850893/142495873-5ab7915a-eb40-4847-9e40-4ba62b0df061.png)

![image](https://user-images.githubusercontent.com/64850893/142496153-e5d450a2-08b8-4fb6-bccd-212e6ff535cf.png)

* Preprocessing Continuous Variables: calculate WOE (Weight of Evidence) and IV (information value), visualizing results, creating dummy variables.

![image](https://user-images.githubusercontent.com/64850893/142496280-b095c837-5ea2-49db-80fe-03194ea152b2.png)

![image](https://user-images.githubusercontent.com/64850893/142496396-1621fbd9-054b-4e02-8766-72a623f00517.png)


## 5.2 Modeling

* Summary table (including p value):

![image](https://user-images.githubusercontent.com/64850893/142500952-42411970-f46c-4abf-a2ec-b522983962a3.png)

* Confusion matrix:

![image](https://user-images.githubusercontent.com/64850893/142500841-4f10af6b-6b01-4842-a7c2-0e60fc7e4f86.png)

* ROC:

![image](https://user-images.githubusercontent.com/64850893/142500749-8210811d-43b0-44c6-8023-4948185b04d6.png)

* Gini:

![image](https://user-images.githubusercontent.com/64850893/142501294-c0cf9d73-03af-40f0-a730-5a4b3441ace0.png)

* Kolmogorov-Smirnov:

![image](https://user-images.githubusercontent.com/64850893/142501341-7d7e1e88-4f52-4474-8dc0-7eeb243878c0.png)

## 5.3 Create a Scorecard

![image](https://user-images.githubusercontent.com/64850893/142501818-37edb173-841f-42b5-bd8d-ff2af5cb093a.png)

![image](https://user-images.githubusercontent.com/64850893/142502352-82e04222-f890-408e-8980-3941b85e2833.png)

## 5.4 Transfer to probability and set the cut-off

![image](https://user-images.githubusercontent.com/64850893/142502545-caf155ac-7d19-4cd6-8ce5-c2fe84990f15.png)

# 6. LGD Model:

## 6.1 Data Prep and EDA

* Similar to the methods in 5.1.

## 6.2 Dependent Varables

* We calculate the dependent variable for the LGD model: recovery rate, which is the ratio of recoveries and funded amount.

## 6.3 Stage 1 - Logistic Regression 

* Summary table：

![image](https://user-images.githubusercontent.com/64850893/142503184-f62bc3b7-e970-490a-9325-6485c1bc2a85.png)

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/64850893/142503593-2bd6013e-f662-41c5-9147-e3c52efa7785.png)

* ROC:

![image](https://user-images.githubusercontent.com/64850893/142503766-64f7b814-8f25-449f-9b86-47802119509f.png)

## 6.4 Stage 2 - Linear Regression

* Summary table:

![image](https://user-images.githubusercontent.com/64850893/142503924-f90d371b-e143-4e00-9d7c-bb73868ba18e.png)

# 7. EAD Model:

## 7.1 Data Prep and EDA

* Similar to the methods in 5.1.

## 7.2 Dependent Varables

* We use the 'CCF' column in the loan_data_defaults data set

## 7.3 Summary table:

![image](https://user-images.githubusercontent.com/64850893/142504336-7f967c73-173f-445e-84fd-b0219cd96a6f.png)


# 8. EL:

* Total Expected Loss:

![image](https://user-images.githubusercontent.com/64850893/142507662-ae2289dd-2ea3-4884-945a-b9acb1c59360.png)

* Total Expected Loss as a proportion of total funded amount for all loans:

![image](https://user-images.githubusercontent.com/64850893/142507782-c918d3e9-dcad-4b1f-803b-a5bb42b148e9.png)


# 9. Conclusion

Given that the ratio of total expected loss and total funded loan is about 7.5%, and  
usually a bank holds 10% of its assets as capital, we can conclude that the level of risk for this bank is relevantly safe.
