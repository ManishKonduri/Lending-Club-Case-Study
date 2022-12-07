# LENDING CLUB CASE STUDY
> Lending club case study for understanding the patterns in loan defaulters via EDA.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Objective : Use EDA to find out the key attributes which will provide the insights for lenders to lend in a safe manner.
- We are using a private Loan data set provided to us

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Observations 
- Loan Purpose
- Employment Length
- Interest Rate
- Annual Income
- Grade and Sub Grade
- Term
- Issued Month and Year
- Verification Status
- Home Ownership
- DTI

## Insights

#### 1. Loan Purpose :-
- small_business -> 27.95 %. (Out of 1624 loans taken by keeping loan purpose as "small_business" 454 loans Charged Off)
- renewable_energy -> 19.14 %. (Out of 94 loans taken by keeping loan purpose as "renewable_energy" 18 loans Charged Off)
- educational -> 17.70 %. (Out of 305 loans taken by keeping loan purpose as "educational" 54 loans Charged Off)

#### 2. Employment Length
The Charged Off Percentage is high for the Loans where the Employment length is greater than equalt to 10+ Years. 
- 10 Years (> 10 Years) -> 16.78 %.
- 7 Years -> 15.28 %.
- 1 Year -> 14.64 %.

#### 3. Interest Rate
Charged Off Percentage is high for Interest Rates :-
- 20-25% -> 39.03 %.
- 15-20% -> 24.46 %.

These are some of the suggested metrics:-

- It is not suggested to provide the loan if the Annual income is 67000 and Interest Rate is between 20 to 25 %
- It is not suggested to provide the loan if the Annual income is 59000 and Interest Rate is between 15 to 20 %
- It is suggested to not to give loans if the people have Funded amount Invested as 35000 and Interest Rate is above 15%

#### 4. Annual Income
Charged Off Percentage is high for Annual Incomes :-
- 0-20k -> 19.9262 %.
- 20k-40k -> 17.6959 %.
- 40k-60k -> 15.4648 %.

These are some of the suggested metrics
- For Annual Income in the range 0k to 20k it is better not to provide loans for the purposes "medical", "renewable_energy", "small_business"
- If the Annual Income is greater than 60,000 and the Interest rate is above 15% then loan is not suggested

#### 5. Grade and Sub Grade
Most of the Charged Off Applicants belong to Grades G,F,E
For Grades G,F the most charged off Sub grades are :- 
- G -> G3, G5
- F -> F4, F5

Grade and Charged Off Percentage are strongly correlated

#### Note :- As the Grade Increases the Charged Off Percentage also increases.

Order -> G,F,E,D,C,B,A

#### 6. Term

For Term, As the Term increases the Charged Off Percentage also Increases

#### 7. Issued Month and Year
- Dec -> 16.3 %.
- Sep -> 16.2 %.
- May -> 16.2 %.

Note :- Although we have plotted graphs for Issued Months, We can ignore those plots because they are the combination of all the years but not one year. So the spread of Issued Month may give us wrong insights

- 2007 -> 17.9 %.
- 2011 -> 16.15 %.
- 2008 -> 15.38 %.

#### 8. Verification Status
Charged Off Percentage is high for the Verification Statuses :- 
- Verified -> 17.33 %.
- Source Verified -> 14.98 %.
- Not Verified -> 12.83 %.

#### 9. Home Ownership
Charged Off Percentage is high for the  Home Ownership values :-
- OTHER -> 17.2 %.
- RENT -> 15.35 %.
- OWN -> 15.21 %.

These are some of the suggested metrics :-

- It is not suggested to provide the loan if the Annual income is 58000 and Home Ownership is of type "OTHER"
- It is not suggested to provide the loan if the Annual income is 49500 and Home Ownership is of type "RENT"
- It is not suggested to provide the loan if the Annual income is 49000 and Home Ownership is of type "OWN"

#### 10. DTI
Charged Off Percentage is high for the DTI values :-
- 20-25 % -> 17.06 %.
- 15-20 % -> 15.76 %.

Note :- There is not much data for 25-30 % group of DTI. SO there is a downwall in the graphs in this region.

Ideally, We can say that there is moderately strong Trend. As DTI Increases the Charged Off Rate increases.

### Insights - Univariate vs Bivariate
- Although we got insights from Univariate analysis at the begining those insight were contridicted when we performed Bivariate analysis
Examples :-
    1. Grades - The Univariate Analysis gave almost the opposite insights of Bivariate Analysis,
    2. Term
    3. Sub Grades,..


## Conclusions
- Less Impact Metrics :-
    - Lower Annual Income, In the range 20,000 to 40,000.
    - Higher Debt to Income Ratio, Betwen 15% - 20%.
    - Higher Loan Amount (Above 15600)
    - Loan Purpose - Education
    - Loan Grade and Subgrade - B and C

- High Impact Metrics :-
    - Loan Grade and Subgrade - Greater than D
    - Loan Purpose - Small Business, Renewable Energy
    - High Interest Rate - above 15%
    - Lower Annual Income - Below 20,000
    
- Combined Impact above metrics :-
    - Home Ownership vs Loan Purpose - Other vs moving, car, small_business
    - Annual Income vs Loan Purpose - 0k to 20k it is better not to provide loans for the purposes "medical", "renewable_energy", "small_business"
    
### Note :- It is better to not to provide loans if the borrower doesn't have data regarding "Annual Income"
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- library - version 1.0
- library - version 2.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@githubusername] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->