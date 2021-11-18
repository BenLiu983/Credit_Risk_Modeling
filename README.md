# Credit_Risk_Modeling

Calculate the amount a specific bank would lose by lending to borrowers using Machine Learning algorithms.

# 1. Objectives

* Investigate the expected credit risk a bank is facing.

# 2. Data

This project is based on a dataset from lending club, consisting loan information from 2007 to 2014 (466k customers * 74 features).

# 3. Methodology

EL = PD * LGD * EAD

* EL: Expected Loss
* PD: Probability of Default (Logistic Regression)
* LGD: Loss Given Default (Linear Regression)
* EAD：Exposure at Default (Linear Regression)


## 4. Variable intepretation:


* Independent variables: first purchase brand, email OR, CTR, coupon redemption rate, enrollment type, enrollment age, baby age, breastfeed type, hospital zone.​

* Machine Learning Models: Logistic regression, decision tree, Artificial Neural Network.​
* 
* Current brand: "1" represents our brand, and other values represent other brands.
* First purchase brand: "1" represents our brand, and other values represent other brands.
* Email OR (open rate): the nubmer of emails opened/the number of emails have been sent to a person
* Email CTR (open rate): the nubmer of emails clicked/the number of emails have been sent to a person
* Coupon redemption rate: the nubmer of coupon redeemed/the number of emails have been sent to a person
* Enrollment type: the source from which a person enroll to our program (Digital Self Enrollment, Co-registered)
* Enrollment age: the age of the baby when the parent enrolled in our program
* Baby age: the age of the babay when the parent took the survey 
* Breastfeed type: "1" represents breastfed only, "2" represents both breastfed and formula feed, "3" represents formula feed only, "4" represents neither.
* Hospital zone: "1" represents our hospital zone, and other values represent other brands.



## 5. PD Model:

## 6. LGD Model:

## 7. EAD Model:

## 8. EL:


