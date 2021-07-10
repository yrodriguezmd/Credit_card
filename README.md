
# Analysis on Customer Profile, Utilization Rates and Attrition Rates among Credit Card Holders

Author:  Maria Rodriguez

Data Source: https://leaps.analyttica.com/sample_cases/11.   There were 23 variables and 101,027 entries, with missing values (<1%) designated as 'Unknown'.  A possible idntifier (Clientnum) was included, and was immediately removed.

This individual analysis was done for purposes of comparing and merging results as part of a group project for the Data Science 2: Statistical Analysis, a course offered by University of Toronto / University of Waterloo, 2021.

The analyses were done in a Jupyter notebook, and utilizes the pandas, numpy, matplotlib, seaborn, scipy, statsmodels and sklearn libraries.  Statistical tests done included t-test, chi-squared, ANOVA, Linear Regression and Logistic Regression.

## Statement of Hypotheses

### Scenario:  Being hired by a bank to determine:

#### A.  The profile of its credit card users
        
        Null hypotheses:
            1.  There is no difference in distribution between male and female customers,
            2.  There is no relationship between age and income among the customers,
            3.  There is no relationship between marital status and income among the customers,
            4.  There is no association between education and income among the customers.
            
#### B.  The most popular credit cards type
        
        Null hypotheses;
            1.  There is no difference in the distribution between the different card types,
            2.  Card type is independent of the customers'
                    a.  age,
                    b.  gender,
                    c.  education,
                    d.  marital status,
                    e.  income
                    
#### C.  Factors associated with high use of credit funds among users
        
        Null hypotheses:
            1.  There is no difference in the amount and number of transaction between genders,
            2.  There is no difference in the number of transactions between different card types,
            3.  There is no relationship between credit limit and utilization ratio
            
#### D.  Predict which users are likely to stay as customers instead of churning
        
        Null hypotheses:
            1.  The outcome of attrition is not affected by any of the base attributes in the dataset, and thus cannot be predicted.


## Summary of Findings and possible Recommendations:

### Customer profile:
    - There is a significantly higher proportion of females among the customers.
    - High-income card owners are older, with a mean age of 47.6 +/- 6.7 (CI 43-53).
    - Low-income is independent of marital status and educational level

-->  Provide bank with background on either increasing the satisfaction by offering female-oriented or older-age oriented rewards, OR by an increased effort to enhance recruitment of males and other-income groups

 ### Credit Card profile:
    -  Blue cards are the most common, followed by Silver, Gold and Platinum.
    -  The card type is independent of age and education
    -  Blue cards are popular with females, married customers, and the low-income group
    -  Silver and Gold cards are popular with males, single customers, and those with annual earnings of 70 thousand dollars and above.
    
-->  Bank can enhance recruitment of credit card owners by offering activities and rewards targeted to females, married people, and offering savings-oriented plans for the low-income group

--> Bank can offer exclusive rewards targeted towards the male population

### Credit Utilization profile
    -  Females make more frequent transactions.
    -  Males make more expensive transactions.
    -  Blue card holders make less frequent transactions.
    -  Credit limits up to around 4 thousand dollars are well utilized, with a sharp decline in utilization beyond 4 thousand.
    
-->  Bank can tailor the benefits of credit card charges (% per use and % of amount payable) to a target population

-->  Bank can gauge the liquidity of their assets by assigning on average 4 thousand credit units per card holder

-->  Banks can offer lower fees for credit use above 4 thousand to increase utilization

### Attrition prediction
    -  Logistic regression analysis showed that Attrition may be predicted by gender, number of dependents, number of products used, transaction count changes and account inactivity. At the 0.5 threshold, the accuracy of predicting attrition is 87&, with an AUC of 0.81.
    
-->  Banks can do a qualification check that includes the above parameters to ascertain good customer retention and minimize churning
-->  Customers who are male, with less dependents, with a high number of bank products used, with increased transaction activity and duration, and with infrequent contacts with the bank, are less liable to attrition.
