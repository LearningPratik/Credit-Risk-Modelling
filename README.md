# Credit-Risk-Modelling

Challenge faced by bank is wrt credit lending

Solution --> How to revise the current credit lending strategy of bank in a more scientific way.

# About dataset
* dataset is from CIBIL Bureau which consists of customers data
* there are 61 independent feature and 1 dependent feature
* dependent feature consists of 4 classes --> P1, P2, P3, P4
* P1 is given to customer with very good credit score
* P2 is given to customer which is good but not as good as P1 and so on.
* Loan is also called TL (Trade line) in bank language.
* Secured loans are something which is backed by a collateral while unsecured is not backed by anything.
* This is why unsecured loans has more interest rates compared to secured loans

# Hypothesis testing

Question - Are these two columns associated ?

* `Null Hypothesis (H0)` --> this two are not associated
* `Alternate Hypothesis (H1)` --> this two are associated

* `Alpha --> significance level`, usually it is 5% or 0.05, This threshold tells us, main kitna galat ho sakta hoon.

* `Confidence level` --> point estimate and margin of error (alpha), 1 - alpha

* We need to find evidence to support the alternate hypothesis which we do using p-value.
* If we don't have enough evidence then we can say that we don't have enough evidence to support alternate hypothesis, and if we have enough evidence then we reject the null hypothesis.

* `p-value` is calculated using tests, tests like t-test, chi-square test, Anova.

* `if p-value <= alpha --> Reject H0 and if p-value >= alpha --> fail to reject the H0`

# TESTS
* <b>Chisquare</b> - categorical v categorical
  
  `Ex : marital status vs loan approved or not`
  
* <b>t-test</b> - categorical v numerical (2 categorical columns) --> only 2 value_counts

  `Ex : Age vs loan approved or not`
  
* <b>ANOVA</b> - categorical v numerical (>=3 categorical columns) --> more than or equal to 3 value_counts

# VIF - Variance inflation factor
* Used to identify multicollinearity
* Takes r-squared value and eliminate if crosses the threshold
* `1/ 1 - r-squared`
* `VIF = 1 --> no multicollinearity`
* `VIF = 1 - 5 --> low multicollinearity`
* `VIF = 5 - 10 --> moderate multicollinearity`
* `VIF > 10 --> High multicollinearity`

# Explaining to Business --> Interpretation of the outcomes

* It depends on Risk appetite
* If Risk appetite is low --> they are not willing to take much risk --> we can say target only P1 customers
* If Risk appetite is high --> they are willing to take risk --> we can say target P1, P2 and maybe P3
