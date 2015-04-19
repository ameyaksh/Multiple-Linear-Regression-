# Multiple-Linear-Regression-
Predicting whether couples would opt for dissolution of marriage by using a logistic regression model

This was one of the case study to work on for the course ECN 525 : Applied Regression Models 

Aim : To predict the probability of couple who opt for dissolution of marriage by using a logistic regression model.

Details of the data set ::

Marriage Dissolution in the U.S.
Data (Divorce2) description:
id: a couple number.
heduc: education of the husband, coded
0 = less than 12 years,
1 = 12 to 15 years, and
2 = 16 or more years.
married: coded 1 have been married before, 0 first marriage
mixed: coded 1 if the husband and wife have different ethnicity (defined as black or other), 0 otherwise.
years: duration of marriage, from the date of wedding to divorce 
div: coded 1 for divorce and 0 for staying married
kids: coded 1 if couple have kids, 0 otherwise
infidelity: coded 1 if there was an adultery, 0 otherwise.

The dataset has 2545 couples 

Questions to answer :


1.	Conduct univariate and bivariate analysis of the data. 
	2. Complete the following table:
      Model     Terms in Model			-2ln L
	Constant only (unadjusted)			
	Years 	
	Years Mixed
	Years Mixed Married 
	Years Mixed Married Kids
	Year  Mixed  Married Heduc  
	Year Mixed  Married  Heduc Mixed*Married


				
	3. What is the odds ratio of divorce for couples who were previously married and married to someone with different race         (married*mixed)? 95% CI? Write the interpretation.
	4. What is the odds ratio of staying married for couples who are married for 10 years and who do not have kids? 95% CI?          Write the interpretation.
5.  Consider a model with ONLY HEDUC  DEBT and YEARS as predictors of divorce. What is the odds of divorce for those couples      in which husbands have less than 13 years of education, have debts and are married for only 2 years? 
	6. whatis the probability that a husband with 16 or more years of education and who has been married before stay married?
	
	7. Report your final model (this should include at least ONE statistical significant interaction). Write the logit       regression model as well as the fitted model. Report and interpret the odds ratios and 95%CI for each predictor of your final model. 
8.	Who’s at the lowest probability of staying married?

Solutions :

Solution 1 :

Univariate Analysis on the data : The average number of years people are married for is 17.5 with the 

median as 13.6 . We observe that couple with as low as 0.1 years of marriage have filed for divorce 

while couple in 73 years of marriage have also filed for divorce. Of the total number of divorces filed, 

in 995 cases the education of husband was less than 12 years, in 1275 cases the education of 

husband was 12 to 15 years while only in 275 cases the education of the husband was more than of 

16 years. Out of the 2545 cases, in 1909 cases couple had the same ethnicity whereas 636 had 

different ethnicity. Out of the 2545 cases filed, 1744 cases did not result in divorce while 801 cases 

resulted in divorce.In case of 696 couples, they were married before while the rest of them, 1850 filed 

for divorce for their first marriage. Assuming debt=1 as yes to financial problems and debt=0 as no 

financial problems then 930 cases didn’t had debt while 1615 cases did have debts.Of all the 2545 

cases, 1375 couples have children while 1170 don’t have them. Of all the 2545 cases, 2309 didn’t 

indulge in adultery while only 236 cases of adultery were reported.

From the Bivariate Analysis of the data we observe that with divorce as our output, we have years, 

mixed and debt (considering their their p-values, debt has just 0.0054 above the level decided of 

0.05, hence considered). Thus, we observe that there is an association between divorce and number 

of years a couple is married for, divorce and if the couple has distinct ethnicity, divorce and the debt 

the couple has.

Solution 2:

Model     Terms in Model -2ln L

A. Constant only (unadjusted): 3170.239 

B. Years: 2844.573 

C. Years Mixed: 2830.293

D. Years Mixed Married: 2815.508

E. Years Mixed Married Kids: 2815.377

F. Year  Mixed  Married Heduc:  2805.087

G. Year Mixed  Married  Heduc Mixed*Married: 2798.319

Solution 3 : Odds ratio is 1.69 with  95% Confidence Interval  [ 1.220, 2.430 ]

Cases who were previously married and married to someone with different race are 1.69 times more 

likely to be divorced than otherwise .As the odds ratio is greater than 1, it signifies that there is a 

possible statistical significance. As the 95% Confidence Interval does not contain the value 1.0, the 

association is statistically significant at  

Solution 4 Odds ratio = 1.9155 Confidence interval: [1.465, 2.504]

Cases who are married for 10 years and who do not have kids are 1.9155 times more likely to stay 

married than otherwise . As the 95% Confidence Interval does’nt contain the value 1.0, the 

association is statistically significant at    

Solution 5: odds of divorce for those couples in which husbands have less than 13 years of 

education, have debts and are married for only 2 years is 1. 07

Solution 6  Probability that a couple with husband with 16 or more years of education and who has 

been married before stays married is 0.72

		


Solution 7: Considering he1 is the dummy variable for heduc=0 (education less than 12 years) and 

he2 is the dummy variable for heduc =1 (education between 12 and 15) and hence we will comparing 

these dummy variable with control group heduc =3 ( education more than 16 years)

Year : the impact of 1 year indicates that for 1 year increase the odds ratio of divorce is 0.929

Mixed : couple who are from different ethnicity are 1.23 times more likely to get divorced than couple 

with same ethnicity

Married : couple who are married before are 0.53 times more likely to get divorced than couple who 

haven’t been married before

mixed*married :couple who are of different ethnicity and have been married before are  2.18 times 

more likely to get divorced than couple who havent been married before and are of same ethnicity

he1 : husband's  who have education less than 12 years are 1.5 times more likely to get divorced 

thhe1an husband's who have education of more than 16 years

he2 :husband's  who have eduaction less than 12 years are 1.10 times more likely to get divorced 

than husband's who have education of more than 16 years

debts : couple who have debts are 1.21 times more likely to get divorced than couple who don’t have 

debts .

Logit model:  Ln(p/(1-p))for Div=βο+β_1 years+β_2 mixed+β_3 married+β_4 mixed*married+β_5 he1+β_6 he2+β_7 debt+ϵ

Fitted model : Ln(p/(1-p))for Div= 0.0237-0.0735years+0.2136mixed-0.6316married+0.5683mixed*married+0.4202he1+0.0958he2+                                         0.1951debt 

Solution 8:

The lowest probability of staying married is for the couple who is just married (0.1 years), who are of 

different ethnicity, have not been previously married, who have debts and where the husband’s 

education was less than 12 years which is 0.30 

This model is dropped because it has 

interaction terms he1*debt , he2*debt which 

are significant



