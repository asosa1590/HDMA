collateralregression <- lm(Collateral ~ Black + Asian +American_Indian_or_Alaska_Native + White + Male + Female + Hispanic_or_Latino + applicant_income_000s + loan_purpose_name + minority_population, data = dfna)

summary(collateralregression)
stargazer(collateralregression, type = 'text')


loanapplicationregression <- lm(Debt_to_income_ratio ~ Black + Asian + American_Indian_or_Alaska_Native+ White + Male+ Female + Hispanic_or_Latino+ applicant_income_000s + loan_purpose_name + minority_population, data=dfna)
summary(loanapplicationregression)
stargazer(loanapplicationregression, type = 'text')


CreditAppRegression <- lm(Credit_app_incomplete ~ Black + Asian + American_Indian_or_Alaska_Native + White + Male+ Female + Hispanic_or_Latino + applicant_income_000s + loan_purpose_name + minority_population, data=dfna)
stargazer(CreditAppRegression, type = 'text')


Purchaserregression <- lm(Loan_Approved ~ purchaser_type_name + hud_median_family_income + Hispanic_or_Latino + Not_Hispanic_or_Latino + American_Indian_or_Alaska_Native + Asian + Black + Native_Hawaiian_or_P.Islander + loan_amount_000s + minority_population )
stargazer(Purchaserregression , type = 'text')


incomeregression <- lm(applicant_income_000s ~ population + minority_population + White + Male + Female + Hispanic_or_Latino + Not_Hispanic_or_Latino + American_Indian_or_Alaska_Native + Asian + Black + Native_Hawaiian_or_P.Islander + purchaser_type_name + loan_purpose_name )
stargazer(incomeregression , type = 'text')


