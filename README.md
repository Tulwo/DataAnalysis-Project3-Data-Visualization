# (Loan data from prosper)
## by (Sharon Tulwo)


## Dataset
> The dataset is Loan data from prosper  
> This is a Loan data set contains 113,937 loans with 81 variables on each loan, including loan original amount, borrower rate , current loan status, borrower income, and many others.  
#### Data wrangling  
> i. Subset the dataset to have columns of intrest and save to a new dataframe df_loans
> ii. select dataset with date from 2009
> iii. find duplicates and nulls from the dataset
>iv. convert datatype to category for all categorical columns
> v. convert datatype to datetime for all date columns

## Summary of Findings
#### Univariant Analysis
> From the LoanStatus Distribution most loans are either in current or completed status. Most loans are performing loans with  few non performing loans.
> DebtToIncome ratio is mostly scattered within the range 10% - 40%. This means that most loans are granted when the DebtToIncome ratio is within the same range
> Most loans borrowers have an income range of 25k-75K. The lower the income range few loans are granted
> Most loans are being held by professionals at 73% with Students at 1% and others as 26%
> The most considered listing category is Debt Consolidation, followed by other, home improvement and business
>The most ideal employment status considered for loan to be granteed is being 'employed' and 'full term'.'Not employed','part time' and 'retired' are either not given loans or they are unlikely to apply for a loan
> The distribution is right skewed with Most members having OriginalLoanAmount less than 5000. As the orginalLoanAmount increases less people qualify for higher Loan amounts
> The Term of over 80% of the loans is 36 months. Almost 20% of the loans are longterm with 60 month. short term lons of 12Months are few.
> The distribution of BorrowerARP is normally disitributed with it peak between 15% and 20% 
> The distribution of BorrowerRate has it peak within 10% to 15%.As the borrower rate increases the number of loan uptake decreased
> Most popular ProsperRating (Alpha) is between A,B,C,D while AA,HR and E are least popular  
> ProsperRating (numeric) is normally distribution, with its peak at 4
> Most loans have a Prosper score of 4,6,8
> Most loan listings have 1 investor. Apart from 1,the other graph is normally distributed.

#### Bivariant
> 1.There is a positive correlation between EstimatedReturn,BorrowerAPR,BorrowerRate and LenderYield  
> 2. ProsperScore has a negative correlation with EstimatedReturn,DebtToIncomrRatio,BorrowerAPR,BorrowerRate and LenderYield. and Positive Correlation to Investors, MothlyLoanPayment, LoanOriginalAmount 
> 3. Investors have a positive correlation with MothlyLoanPayment, LoanOriginalAmount and ProsperScore
> 4. The higher the income the higher the number of goodloans. With low income the higher the number of bad loans,as the ratio of good to bad loans increases  
> 5. BadLoans have a higher BorrowerRate than GoodLoans
> 6. BorrowerAPR is the highest where employment status is not employed.Those employed have a lower borrower rate
> 7. Prosper score is higher at 7 when income range is highest(100,000+). With low Prosper score of 5 where income is less than 50,000

#### Multivariant
> 1. All badLoans have a higher BorrowerAPR in all Employment status categories
> 2. The higher the LoanOriginalAmount the higher the Term in all IncomeRanges. Long term loans are more where income range is higher and loan amount increases
> 3. The higher the prosper rating the Lower the DebtToIncome ratio
> 4. The Better or higher the prosper Score yields lower Borrower rates. On all prosper Score categories the bad loans have a higher Borrower rate
> 5. As the Term period decreases the Monthly Loan Payment Variable Increases. As the LoanOriginalAmount increases the Term period increases

## Key Insights for Presentation
> A. The relationship between quantitative variables of interest show that:
> i. ProsperScore has a negative correlation with EstimatedReturn,DebtToIncomeRatio,BorrowerAPR,BorrowerRate,LenderYield. And Positive Correlation to Investors, MothlyLoanPayment, LoanOriginalAmount  
> ii. There is a positive correlation between EstimatedReturn,BorrowerAPR,BorrowerRate and LenderYield  
> iii. Investors have a positive correlation with MothlyLoanPayment, LoanOriginalAmount and ProsperScore  
> B. How the cost of loan and capacity of loan uptake affects the status of the loan.  
> i. All badLoans with LoanStatus as (Chargedoff,PastDue,Defaulted) have  higher BorrowerAPR across all EmploymentStatus categories  
> ii. The EmploymentStatus, Not-employed has the highest BorrowerAPR. This show that its more risky   
> C.  How the cost of loan and credit score affect the status of the loan:   
> i. The Better or higher the prosper Score yields lower Borrower rates.      
>ii. on all prosper Score categories the bad loans have a higher Borrower rate    
> When the Cost of loan is higher and the credit Score is bad the Loan status type results to badloan  
D. What is the relationship on LoanOriginalAmount, MonthlyLoanPayment and Term:  
> i.  As the Term period decreases the Monthly Loan Payment Variable Increases.  
> ii. As the LoanOriginalAmount increases the Term period increases  
> The Term of the loans is calculated based on the loanOriginalAmount and the MonthlyLoanPayment  
