# Lending Club Case Study
> Helping Largest Online marketplace facilitating loans to identify risky loan applicants, thereby minimizing credit loss


## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Assumptions](#assumptions)
## General Information
### Background
We assume we work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
- If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
- If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company


The dataset considered contains the information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.

 
In this case study, we will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.

When a person applies for a loan, there are two types of decisions that could be taken by the company:
1. **Loan accepted**: If the company approves the loan, there are 3 possible scenarios described below:
    1. **Fully paid**: Applicant has fully paid the loan (the principal and the interest rate).
    2. **Current**: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.
    3. **Charged-off**: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan 
2. **Loan rejected**: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### Business Problem

This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface. 

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). The credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'. 

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the **driving factors (or driver variables)** behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment. 


## Conclusions
- Applicants who opted for higher term (60 months) tend to default more than others. 
- Applicants who got loan for higher interest rate tend to default more than others.
- Applicants with home ownership as “OTHER” tend to default more likely than rest of the categories. Also, there are no defaulters in category “NONE”
- Surprisingly, Loan Applications whose Income is verified defaults more than others by at least 2%. May be verification process needs to be revisited. 
- Applicants whose purpose of loan is “educational” or “small business” tend to default more than other categories by huge difference between 8 % - 17 %. 
- Applicants whose employment length is missing also shows similar pattern for 60 months
- Applicants with 60 months term and verification status as “Source Verified” and “Verified” tend to default more than other combinations
- Applicants with no employment length specified tend to default more for educational purpose


### Note:
```
Some analyses like univarate analysis on funded amount, interest rate, segmented univariate analysis using open credit lines, bivariate analysis of term vs interest rate are removed to maintain conciseness as they didn't yield meaningful outcomes
```

## Technologies Used
 
Python 3.x

### Python Libraries
- pandas - version 1.1.4
- matplotlib - version 3.5.1
- seaborn - version 0.11.2

## Assumptions
- funded_amnt_inv is already included in funded_amnt. Hence, funded_amnt_inv is ignored for the analysis
- Applicants with loan status as current are removed for the analysis as they are not clear indicators of defaulters or not. 


## Contact
Created by [@sowmya690](https://github.com/sowmya690) feel free to contact!
