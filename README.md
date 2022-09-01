# Prosper Loan Data Exploration

## Dataset

The dataset consists of information on loan request from <a href="https://www.prosper.com/">Prosper.com</a>. Comprises 113,937 unique listings with 81 variables giving information about the borrower and the loan requested for. The dataset can be downloaded from <a href="https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000">here</a> or can be requested using Prosper API key with the data dictionary available <a href="https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv&sa=D&ust=1554482573645000">here.</a>

For this analysis all 81 variables were not used but 38 variables were selected and 29,955 rows were dropped due to null values in the Prosper Rating column, an extra column(AnnualIncome) was added by multiplying values in MonthlyIncome by 12

The variables used are;
* ListingCreationDate
* ListingCategory (numeric)
* BorrowerState
* Occupation
* IsBorrowerHomeowner
* EmploymentStatus
* EmploymentStatusDuration
* StatedMonthlyIncome
* AnnnualIncome
* IncomeRange
* IncomeVerifiable
* DebtToIncomeRatio
* DateCreditPulled
* CreditScoreRangeLower
* CreditScoreRangeUpper
* ProsperScore
* ProsperRating (numeric)
* ProsperRating (Alpha)
* CurrentDelinquencies
* AmountDelinquent
* CurrentCreditLines 
* OpenCreditLines
* OpenRevolvingMonthlyPayment
* RevolvingCreditBalance     
* LoanOriginationDate          
* LoanOriginalAmount        
* Term                         
* MonthlyLoanPayment           
* BorrowerRate                 
* BorrowerAPR                  
* EstimatedEffectiveYield      
* EstimatedLoss                
* EstimatedReturn            
* LenderYield                  
* Recommendations             
* Investors                    
* LoanStatus  
* ClosedDate


## Summary of Findings

In the exploration, I was very intersted in the Prosper Rating and what it affects and what also affects it.

I found out that it is of added advantage for a Borrower to have a good Prosper Rating as it helps in the interest rate (the better the rating the lower the interest rate) and the number of investors willing to invest in a loan (more investors for better ratings). These ratings also determine how high a borrower can decide to borrow(most high loan amount are from those with good rating). 

In this analysis it shows the rating is affected by the amount of delinquent(good rating has low amount delinquent), current credit lines(good ratings have high current credit lines) and revolving credit balance(good ratings have high revolving credit balance) of the borrower, the annual income as those with high income have very good rating, the borrower being a home owner(most people who good ratings are home owners) and the debt to income ratio(lower for good ratings).

Those with good rating are mostly seen to fall into the loan status category of Completed and Current

Considering the information of the Borrower, I found out that California requests for loans alot but Washington DC though not requesting alot, request for the highest amount of loans and most of the loans requested for are for Debt consolidation. It is quite expected that the analysis shows that loan is mostly requested by the employed and those with high income range request for higher amount of loans as compared to those with lower income range.

Other variables considered, the lender yield which is proportional to the interest rate and the monthly payment which increases with the loan amount. Also, the duration of the loan(Term) most times is higher with high amount of loan but with a lower interest rate and for this reason we also see that the number of investors reduce with an increase in the loan term.

## Key Insights for Presentation

For the presentation, my focus is on everything related to the rating like the benefit of having a good rating, what could help give a good rating. I have left out most of the intermediate derivations. 

I start by looking at the benefit, first of introducing the **loan amount** variable showing the distribution and then a lineplot to show the relationship. I move on to the **interest rate** variable showing the distribution of interest rate then use the violinplot to show how it is affected by prosper rating. Afterwards, I introduce the next variable which is the **investors**, I use boxplot to show how it affects the number of investors for a loan

Then I look at what could bring about good/poor prosper rating using line plots to look at variables like **annual income**, **amount delinquent**, **current credit lines**, **revolving credit balance**, **is borrower home owner**, **debt to income ratio**
