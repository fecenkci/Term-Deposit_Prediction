## Project Objective:

### The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).

### Data Set Information:

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

There are four datasets:
1. bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010), very close to the data analyzed in [Moro et al., 2014]
2. bank-additional.csv with 10% of the examples (4119), randomly selected from bank-additional-full.csv, and 20 inputs.

#### What Is a Term Deposit?

- A term deposit is a type of deposit account held at a financial institution where money is locked up for some set period of time.
- Term deposits are usually short-term deposits with maturities ranging from one month to a few years.
- Typically, term deposits offer higher interest rates than traditional liquid savings accounts, whereby customers can withdraw their money at any time.

#### Term Deposit Explained.

When an account holder deposits funds at a bank, the bank can use that money to lend to other consumers or businesses. In return for the right to use these funds for lending, they will pay the depositor compensation in the form of interest on the account balance. With most deposit accounts of this nature, the owner may withdraw their money at any time. This makes it difficult for the bank to know ahead of time how much they may lend at any given time.

To overcome this problem, banks offer term deposit accounts. A customer will deposit or invest in one of these accounts, agreeing not to withdraw their funds for a fixed period in return for a higher rate of interest paid on the account.

The interest earned on a term deposit account is slightly higher than that paid on standard savings or interest-bearing checking accounts. The increased rate is because access to the money is limited for the timeframe of the term deposit. Term deposits are an extremely safe investment and are therefore very appealing to conservative, low-risk investors. 

| Pros | Cons|
|------|-----|
|Term deposits offer a fixed rate of interest over the life of the investment.|Interest rates paid on term deposits are typically lower or less attractive than most fixed-rate investments.|
|Term deposits are risk-free, safe investments since they're either backed by the FDIC or the NCUA.|Term deposits can't be withdrawn early without penalty or losing all of the interest earned.|
|Various maturities allow investors to stagger end-dates to create an investment ladder.|Interest rates don't keep up with rising inflation.|
|Term deposits have a low minimum deposit amount.|Interest rate risk exists if investors are locked in a low-rate term deposit while overall interest rates are rising.|
|Term deposits pay higher rates for larger initial deposit amounts.|-|

## Input variables:

### Bank client data:
1. age (numeric)
2. job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
3. marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4. education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
5. default: has credit in default? (categorical: 'no','yes','unknown')
6. housing: has housing loan? (categorical: 'no','yes','unknown')
7. loan: has personal loan? (categorical: 'no','yes','unknown')

### Related with the last contact of the current campaign:
8. contact: contact communication type (categorical: 'cellular','telephone')
9. month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10. day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11. duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

### Other attributes:
12. campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13. pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14. previous: number of contacts performed before this campaign and for this client (numeric)
15. poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

#### Social and economic context attributes:
16. emp.var.rate: employment variation rate - quarterly indicator (numeric)
17. cons.price.idx: consumer price index - monthly indicator (numeric)
18. cons.conf.idx: consumer confidence index - monthly indicator (numeric)
19. euribor3m: euribor 3 month rate - daily indicator (numeric)
20. nr.employed: number of employees - quarterly indicator (numeric)

Output variable (desired target):
21. y - has the client subscribed a term deposit? (binary: 'yes','no')

#### WHO  =  BANK'S CUSTOMERS
#### WHAT  =  bank.columns
#### WHEN  =  BETWEEN MAY 08 AND NOV 10
#### WHERE  =  PORTUGAL
#### HOW  =  BANK'S TELEMARKETING RECORDS
#### WHY  =  PREDICT WHETHER CUSTOMERS WILL SUBSCRIBE TO TERM DEPOSIT OR NOT
