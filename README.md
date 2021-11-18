# Credit_Risk_Modeling

Calculate the amount a specific bank would lose by lending to borrowers using Machine Learning algorithms.

# 1. Objectives

Investigate the expected credit risk a bank is facing.

# 2. Data

This project is based on a dataset from lending club, consisting loan information from 2007 to 2014 (466k customers * 75 features).

# 3. Methodology

EL = PD * LGD * EAD

* EL (Expected Loss): The amount a lender might lose by lending to a borrower.
* PD (Probability of Default): The borrowers inability to repay their debt in full or on time (Logistic Regression).
* LGD (Loss Given Default): The proportion of the total exposure that cannot be recovered by the lender once a default has occurred (Linear Regression).
* EAD (Exposure at Default): The total value that a lender is exposed to when a borrower defaults (Linear Regression).

## 4. Variable intepretation:

![image](https://user-images.githubusercontent.com/64850893/142494442-c3d93b5a-90d6-4a7b-a187-aaac1975296d.png)

![image](https://user-images.githubusercontent.com/64850893/142494551-9060105e-60a6-46bc-84ab-1ac4f3b8ebcc.png)



## 5. PD Model:

### 5.1 Data Prep

* Dependent Variable: Good/ Bad (Default) Definition. Default and Non-default Accounts.

* Preprocessing Discrete Variables: calculate WOE (Weight of Evidence) and IV (information value), visualizing Results, creating Dummy Variables.

![image](https://user-images.githubusercontent.com/64850893/142495873-5ab7915a-eb40-4847-9e40-4ba62b0df061.png)

![image](https://user-images.githubusercontent.com/64850893/142496153-e5d450a2-08b8-4fb6-bccd-212e6ff535cf.png)

* Preprocessing Continuous Variables: calculate WOE (Weight of Evidence) and IV (information value), visualizing Results, creating Dummy Variables.

![image](https://user-images.githubusercontent.com/64850893/142496280-b095c837-5ea2-49db-80fe-03194ea152b2.png)

![image](https://user-images.githubusercontent.com/64850893/142496396-1621fbd9-054b-4e02-8766-72a623f00517.png)


### 5.2 Modeling (p value)




## 6. LGD Model:

## 7. EAD Model:

## 8. EL:


