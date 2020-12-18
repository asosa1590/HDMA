
````

# HDMA
Code for Project 
# Co-Applicant Name
dfna$Hispanic_or_Latino <- ifelse(dfna$co_applicant_ethnicity_name == 'Hispanic or Latino', 1, 0)
dfna$Not_Hispanic_or_Latino<- ifelse(dfna$co_applicant_ethnicity_name == 'Not Hispanic or Latino', 1, 0)
dfna$Asian <-ifelse(dfna$co_applicant_ethnicity_name =='Asian',1,0)
dfna$Native_Hawaiian_or_P.Islander <-ifelse(dfna$co_applicant_ethnicity_name =='Native Hawaiian or Other Pacific Islander',1,0)
dfna$Male<-ifelse(dfna$co_applicant_sex_name =='Male',1,0)
dfna$Female<-ifelse(dfna$co_applicant_sex_name =='Female',1,0)

SubsetData1 <- subset(dat2, select = agency_name,loan_type_name,property_type_name, loan_purpose_name, owner_occupancy_name ,loan_amount_000s, preapproval_name, action_taken_name, msamd_name, county_name, applicant_ethnicity_name, co_applicant_ethnicity_name, applicant_race_name_1, co_applicant_race_name_1, applicant_sex_name, co_applicant_sex_name, applicant_income_000s, purchaser_type_name, denial_reason_name_1 , hoepa_status_name, lien_status_name ,population, minority_population ,hud_median_family_income , number_of_owner_occupied_units, number_of_1_to_4_family_units)


> x<-lm(Collateral~Black+ Asian + American_Indian_or_Alaska_Native + White + Male + Female + Hispanic_or_Latino + applicant_income_000s +loan_purpose_name +county_name + minority_population,data=dfna)

Call:
lm(formula = Collateral ~ Black + Asian + American_Indian_or_Alaska_Native + 
    White + Male + Female + Hispanic_or_Latino + applicant_income_000s + 
    loan_purpose_name + county_name + minority_population, data = dfna)

Residuals:
     Min       1Q   Median       3Q      Max 
-0.07726 -0.03091 -0.02182 -0.01313  0.99943 

Coefficients:
                                   Estimate Std. Error
(Intercept)                       2.840e-02  2.067e-03
Black                            -3.321e-03  1.421e-03
Asian                            -4.298e-03  1.400e-03
American_Indian_or_Alaska_Native -3.102e-03  3.762e-03
White                            -9.747e-03  1.089e-03
Male                             -4.672e-04  1.275e-03
Female                           -2.724e-04  1.307e-03
Hispanic_or_Latino                3.695e-03  1.028e-03
applicant_income_000s             2.782e-05  5.125e-06
loan_purpose_nameHome purchase   -5.884e-03  8.201e-04
loan_purpose_nameRefinancing      1.242e-02  8.591e-04
county_nameAllegany County        1.202e-02  5.106e-03
county_nameBronx County           1.221e-03  2.433e-03
county_nameBroome County         -2.107e-03  2.940e-03
county_nameCattaraugus County     1.036e-02  4.292e-03
county_nameCayuga County          3.286e-03  3.828e-03
county_nameChautauqua County      1.216e-02  3.516e-03
county_nameChemung County        -2.442e-03  3.590e-03
county_nameChenango County        1.721e-02  5.104e-03
county_nameClinton County         1.329e-02  4.020e-03
county_nameColumbia County        1.189e-03  3.974e-03
county_nameCortland County        8.767e-03  5.000e-03
county_nameDelaware County        1.688e-02  4.920e-03
county_nameDutchess County        3.927e-03  2.416e-03
county_nameErie County           -4.363e-03  1.990e-03
county_nameEssex County           1.211e-02  4.992e-03
county_nameFranklin County        1.248e-02  5.137e-03
county_nameFulton County          1.099e-02  4.639e-03
county_nameGenesee County         9.108e-03  4.579e-03
county_nameGreene County          5.585e-03  4.152e-03
county_nameHamilton County        2.359e-02  1.067e-02
county_nameHerkimer County        1.225e-02  3.752e-03
county_nameJefferson County       8.441e-03  3.189e-03
county_nameKings County          -8.985e-03  2.046e-03
county_nameLewis County           4.056e-04  5.499e-03
county_nameLivingston County     -5.598e-05  4.108e-03
county_nameMadison County         6.425e-03  3.874e-03
county_nameMonroe County         -1.105e-02  2.010e-03
county_nameMontgomery County      1.417e-02  4.931e-03
county_nameNassau County         -1.416e-02  1.923e-03
county_nameNew York County        4.852e-04  2.347e-03
county_nameNiagara County        -4.895e-04  2.711e-03
county_nameOneida County         -8.853e-04  2.530e-03
county_nameOnondaga County       -6.089e-03  2.174e-03
county_nameOntario County        -2.694e-03  3.020e-03
county_nameOrange County          4.022e-03  2.271e-03
county_nameOrleans County         7.066e-03  5.253e-03
county_nameOswego County          2.649e-03  3.164e-03
county_nameOtsego County          1.495e-02  4.505e-03
county_namePutnam County         -1.821e-03  3.344e-03
county_nameQueens County         -1.128e-02  2.028e-03
county_nameRensselaer County      8.681e-03  2.868e-03
county_nameRichmond County       -1.142e-02  2.212e-03
county_nameRockland County       -7.772e-03  2.484e-03
county_nameSaratoga County       -6.505e-03  2.419e-03
county_nameSchenectady County     7.413e-03  2.864e-03
county_nameSchoharie County       1.600e-02  5.442e-03
county_nameSchuyler County        1.581e-02  6.541e-03
county_nameSeneca County          1.156e-02  5.409e-03
county_nameSt. Lawrence County    2.779e-02  3.950e-03
county_nameSteuben County        -3.784e-04  3.332e-03
county_nameSuffolk County        -7.947e-03  1.870e-03
county_nameSullivan County        2.223e-02  3.942e-03
county_nameTioga County           5.156e-03  4.590e-03
county_nameTompkins County       -7.201e-03  4.120e-03
county_nameUlster County          7.903e-03  2.866e-03
county_nameWarren County         -1.370e-03  3.699e-03
county_nameWashington County      2.728e-02  4.028e-03
county_nameWayne County          -4.146e-03  3.258e-03
county_nameWestchester County    -3.763e-03  2.054e-03
county_nameWyoming County         6.876e-03  5.050e-03
county_nameYates County          -4.731e-04  5.810e-03
minority_population               6.757e-05  1.330e-05
                                 t value Pr(>|t|)    
(Intercept)                       13.737  < 2e-16 ***
Black                             -2.338 0.019409 *  
Asian                             -3.070 0.002144 ** 
American_Indian_or_Alaska_Native  -0.825 0.409587    
White                             -8.948  < 2e-16 ***
Male                              -0.366 0.714053    
Female                            -0.208 0.834846    
Hispanic_or_Latino                 3.595 0.000324 ***
applicant_income_000s              5.430 5.65e-08 ***
loan_purpose_nameHome purchase    -7.174 7.29e-13 ***
loan_purpose_nameRefinancing      14.457  < 2e-16 ***
county_nameAllegany County         2.355 0.018534 *  
county_nameBronx County            0.502 0.615766    
county_nameBroome County          -0.717 0.473554    
county_nameCattaraugus County      2.413 0.015821 *  
county_nameCayuga County           0.858 0.390663    
county_nameChautauqua County       3.460 0.000541 ***
county_nameChemung County         -0.680 0.496347    
county_nameChenango County         3.372 0.000746 ***
county_nameClinton County          3.307 0.000943 ***
county_nameColumbia County         0.299 0.764804    
county_nameCortland County         1.753 0.079531 .  
county_nameDelaware County         3.431 0.000602 ***
county_nameDutchess County         1.626 0.104016    
county_nameErie County            -2.193 0.028311 *  
county_nameEssex County            2.427 0.015231 *  
county_nameFranklin County         2.429 0.015122 *  
county_nameFulton County           2.368 0.017862 *  
county_nameGenesee County          1.989 0.046695 *  
county_nameGreene County           1.345 0.178555    
county_nameHamilton County         2.210 0.027129 *  
county_nameHerkimer County         3.265 0.001095 ** 
county_nameJefferson County        2.647 0.008117 ** 
county_nameKings County           -4.392 1.13e-05 ***
county_nameLewis County            0.074 0.941201    
county_nameLivingston County      -0.014 0.989129    
county_nameMadison County          1.658 0.097266 .  
county_nameMonroe County          -5.498 3.85e-08 ***
county_nameMontgomery County       2.873 0.004062 ** 
county_nameNassau County          -7.364 1.80e-13 ***
county_nameNew York County         0.207 0.836241    
county_nameNiagara County         -0.181 0.856689    
county_nameOneida County          -0.350 0.726430    
county_nameOnondaga County        -2.801 0.005097 ** 
county_nameOntario County         -0.892 0.372346    
county_nameOrange County           1.771 0.076538 .  
county_nameOrleans County          1.345 0.178587    
county_nameOswego County           0.837 0.402511    
county_nameOtsego County           3.319 0.000904 ***
county_namePutnam County          -0.544 0.586122    
county_nameQueens County          -5.559 2.72e-08 ***
county_nameRensselaer County       3.027 0.002470 ** 
county_nameRichmond County        -5.164 2.42e-07 ***
county_nameRockland County        -3.129 0.001756 ** 
county_nameSaratoga County        -2.689 0.007163 ** 
county_nameSchenectady County      2.589 0.009632 ** 
county_nameSchoharie County        2.940 0.003282 ** 
county_nameSchuyler County         2.416 0.015672 *  
county_nameSeneca County           2.137 0.032580 *  
county_nameSt. Lawrence County     7.037 1.97e-12 ***
county_nameSteuben County         -0.114 0.909565    
county_nameSuffolk County         -4.249 2.14e-05 ***
county_nameSullivan County         5.639 1.71e-08 ***
county_nameTioga County            1.123 0.261316    
county_nameTompkins County        -1.748 0.080533 .  
county_nameUlster County           2.757 0.005829 ** 
county_nameWarren County          -0.371 0.711000    
county_nameWashington County       6.773 1.26e-11 ***
county_nameWayne County           -1.273 0.203136    
county_nameWestchester County     -1.832 0.067001 .  
county_nameWyoming County          1.362 0.173279    
county_nameYates County           -0.081 0.935095    
minority_population                5.080 3.77e-07 ***
---
Signif. codes:  
0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.1501 on 361612 degrees of freedom
Multiple R-squared:  0.006085,	Adjusted R-squared:  0.005887 
F-statistic: 30.75 on 72 and 361612 DF,  p-value: < 2.2e-16

> save(dfna,file = "HDMA2017AS.Rdata")
> summary(x)

Call:
lm(formula = Collateral ~ Black + Asian + American_Indian_or_Alaska_Native + 
    White + Male + Female + Hispanic_or_Latino + applicant_income_000s + 
    loan_purpose_name + county_name + minority_population, data = dfna)

Residuals:
     Min       1Q   Median       3Q      Max 
-0.07726 -0.03091 -0.02182 -0.01313  0.99943 

Coefficients:
                                   Estimate Std. Error
(Intercept)                       2.840e-02  2.067e-03
Black                            -3.321e-03  1.421e-03
Asian                            -4.298e-03  1.400e-03
American_Indian_or_Alaska_Native -3.102e-03  3.762e-03
White                            -9.747e-03  1.089e-03
Male                             -4.672e-04  1.275e-03
Female                           -2.724e-04  1.307e-03
Hispanic_or_Latino                3.695e-03  1.028e-03
applicant_income_000s             2.782e-05  5.125e-06
loan_purpose_nameHome purchase   -5.884e-03  8.201e-04
loan_purpose_nameRefinancing      1.242e-02  8.591e-04
county_nameAllegany County        1.202e-02  5.106e-03
county_nameBronx County           1.221e-03  2.433e-03
county_nameBroome County         -2.107e-03  2.940e-03
county_nameCattaraugus County     1.036e-02  4.292e-03
county_nameCayuga County          3.286e-03  3.828e-03
county_nameChautauqua County      1.216e-02  3.516e-03
county_nameChemung County        -2.442e-03  3.590e-03
county_nameChenango County        1.721e-02  5.104e-03
county_nameClinton County         1.329e-02  4.020e-03
county_nameColumbia County        1.189e-03  3.974e-03
county_nameCortland County        8.767e-03  5.000e-03
county_nameDelaware County        1.688e-02  4.920e-03
county_nameDutchess County        3.927e-03  2.416e-03
county_nameErie County           -4.363e-03  1.990e-03
county_nameEssex County           1.211e-02  4.992e-03
county_nameFranklin County        1.248e-02  5.137e-03
county_nameFulton County          1.099e-02  4.639e-03
county_nameGenesee County         9.108e-03  4.579e-03
county_nameGreene County          5.585e-03  4.152e-03
county_nameHamilton County        2.359e-02  1.067e-02
county_nameHerkimer County        1.225e-02  3.752e-03
county_nameJefferson County       8.441e-03  3.189e-03
county_nameKings County          -8.985e-03  2.046e-03
county_nameLewis County           4.056e-04  5.499e-03
county_nameLivingston County     -5.598e-05  4.108e-03
county_nameMadison County         6.425e-03  3.874e-03
county_nameMonroe County         -1.105e-02  2.010e-03
county_nameMontgomery County      1.417e-02  4.931e-03
county_nameNassau County         -1.416e-02  1.923e-03
county_nameNew York County        4.852e-04  2.347e-03
county_nameNiagara County        -4.895e-04  2.711e-03
county_nameOneida County         -8.853e-04  2.530e-03
county_nameOnondaga County       -6.089e-03  2.174e-03
county_nameOntario County        -2.694e-03  3.020e-03
county_nameOrange County          4.022e-03  2.271e-03
county_nameOrleans County         7.066e-03  5.253e-03
county_nameOswego County          2.649e-03  3.164e-03
county_nameOtsego County          1.495e-02  4.505e-03
county_namePutnam County         -1.821e-03  3.344e-03
county_nameQueens County         -1.128e-02  2.028e-03
county_nameRensselaer County      8.681e-03  2.868e-03
county_nameRichmond County       -1.142e-02  2.212e-03
county_nameRockland County       -7.772e-03  2.484e-03
county_nameSaratoga County       -6.505e-03  2.419e-03
county_nameSchenectady County     7.413e-03  2.864e-03
county_nameSchoharie County       1.600e-02  5.442e-03
county_nameSchuyler County        1.581e-02  6.541e-03
county_nameSeneca County          1.156e-02  5.409e-03
county_nameSt. Lawrence County    2.779e-02  3.950e-03
county_nameSteuben County        -3.784e-04  3.332e-03
county_nameSuffolk County        -7.947e-03  1.870e-03
county_nameSullivan County        2.223e-02  3.942e-03
county_nameTioga County           5.156e-03  4.590e-03
county_nameTompkins County       -7.201e-03  4.120e-03
county_nameUlster County          7.903e-03  2.866e-03
county_nameWarren County         -1.370e-03  3.699e-03
county_nameWashington County      2.728e-02  4.028e-03
county_nameWayne County          -4.146e-03  3.258e-03
county_nameWestchester County    -3.763e-03  2.054e-03
county_nameWyoming County         6.876e-03  5.050e-03
county_nameYates County          -4.731e-04  5.810e-03
minority_population               6.757e-05  1.330e-05
                                 t value Pr(>|t|)    
(Intercept)                       13.737  < 2e-16 ***
Black                             -2.338 0.019409 *  
Asian                             -3.070 0.002144 ** 
American_Indian_or_Alaska_Native  -0.825 0.409587    
White                             -8.948  < 2e-16 ***
Male                              -0.366 0.714053    
Female                            -0.208 0.834846    
Hispanic_or_Latino                 3.595 0.000324 ***
applicant_income_000s              5.430 5.65e-08 ***
loan_purpose_nameHome purchase    -7.174 7.29e-13 ***
loan_purpose_nameRefinancing      14.457  < 2e-16 ***
county_nameAllegany County         2.355 0.018534 *  
county_nameBronx County            0.502 0.615766    
county_nameBroome County          -0.717 0.473554    
county_nameCattaraugus County      2.413 0.015821 *  
county_nameCayuga County           0.858 0.390663    
county_nameChautauqua County       3.460 0.000541 ***
county_nameChemung County         -0.680 0.496347    
county_nameChenango County         3.372 0.000746 ***
county_nameClinton County          3.307 0.000943 ***
county_nameColumbia County         0.299 0.764804    
county_nameCortland County         1.753 0.079531 .  
county_nameDelaware County         3.431 0.000602 ***
county_nameDutchess County         1.626 0.104016    
county_nameErie County            -2.193 0.028311 *  
county_nameEssex County            2.427 0.015231 *  
county_nameFranklin County         2.429 0.015122 *  
county_nameFulton County           2.368 0.017862 *  
county_nameGenesee County          1.989 0.046695 *  
county_nameGreene County           1.345 0.178555    
county_nameHamilton County         2.210 0.027129 *  
county_nameHerkimer County         3.265 0.001095 ** 
county_nameJefferson County        2.647 0.008117 ** 
county_nameKings County           -4.392 1.13e-05 ***
county_nameLewis County            0.074 0.941201    
county_nameLivingston County      -0.014 0.989129    
county_nameMadison County          1.658 0.097266 .  
county_nameMonroe County          -5.498 3.85e-08 ***
county_nameMontgomery County       2.873 0.004062 ** 
county_nameNassau County          -7.364 1.80e-13 ***
county_nameNew York County         0.207 0.836241    
county_nameNiagara County         -0.181 0.856689    
county_nameOneida County          -0.350 0.726430    
county_nameOnondaga County        -2.801 0.005097 ** 
county_nameOntario County         -0.892 0.372346    
county_nameOrange County           1.771 0.076538 .  
county_nameOrleans County          1.345 0.178587    
county_nameOswego County           0.837 0.402511    
county_nameOtsego County           3.319 0.000904 ***
county_namePutnam County          -0.544 0.586122    
county_nameQueens County          -5.559 2.72e-08 ***
county_nameRensselaer County       3.027 0.002470 ** 
county_nameRichmond County        -5.164 2.42e-07 ***
county_nameRockland County        -3.129 0.001756 ** 
county_nameSaratoga County        -2.689 0.007163 ** 
county_nameSchenectady County      2.589 0.009632 ** 
county_nameSchoharie County        2.940 0.003282 ** 
county_nameSchuyler County         2.416 0.015672 *  
county_nameSeneca County           2.137 0.032580 *  
county_nameSt. Lawrence County     7.037 1.97e-12 ***
county_nameSteuben County         -0.114 0.909565    
county_nameSuffolk County         -4.249 2.14e-05 ***
county_nameSullivan County         5.639 1.71e-08 ***
county_nameTioga County            1.123 0.261316    
county_nameTompkins County        -1.748 0.080533 .  
county_nameUlster County           2.757 0.005829 ** 
county_nameWarren County          -0.371 0.711000    
county_nameWashington County       6.773 1.26e-11 ***
county_nameWayne County           -1.273 0.203136    
county_nameWestchester County     -1.832 0.067001 .  
county_nameWyoming County          1.362 0.173279    
county_nameYates County           -0.081 0.935095    
minority_population                5.080 3.77e-07 ***
---
Signif. codes:  
0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.1501 on 361612 degrees of freedom
Multiple R-squared:  0.006085,	Adjusted R-squared:  0.005887 
F-statistic: 30.75 on 72 and 361612 DF,  p-value: < 2.2e-16




 purchaserregression <- lm(Loan_Approved ~ purchaser_type_name + hud_median_family_income + Hispanic_or_Latino + Not_Hispanic_or_Latino + American_Indian_or_Alaska_Native + Asian + Black + Native_Hawaiian_or_P.Islander + loan_amount_000s + minority_population )
> summary(purchaserregression)

Call:
lm(formula = Loan_Approved ~ purchaser_type_name + hud_median_family_income + 
    Hispanic_or_Latino + Not_Hispanic_or_Latino + American_Indian_or_Alaska_Native + 
    Asian + Black + Native_Hawaiian_or_P.Islander + loan_amount_000s + 
    minority_population)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.12090 -0.37990 -0.00022  0.30787  1.08219 

Coefficients:
                                                                                                  Estimate
(Intercept)                                                                                      8.089e-01
purchaser_type_nameCommercial bank, savings bank or savings association                          1.336e-01
purchaser_type_nameFannie Mae (FNMA)                                                            -4.239e-02
purchaser_type_nameFarmer Mac (FAMC)                                                             1.028e-01
purchaser_type_nameFreddie Mac (FHLMC)                                                          -4.475e-02
purchaser_type_nameGinnie Mae (GNMA)                                                            -7.123e-02
purchaser_type_nameLife insurance company, credit union, mortgage bank, or finance company       1.277e-01
purchaser_type_nameLoan was not originated or was not sold in calendar year covered by register -4.791e-01
purchaser_type_nameOther type of purchaser                                                       1.091e-01
purchaser_type_namePrivate securitization                                                        4.620e-02
hud_median_family_income                                                                        -1.254e-06
Hispanic_or_Latino                                                                               1.720e-01
Not_Hispanic_or_Latino                                                                           2.242e-01
American_Indian_or_Alaska_Native                                                                -5.532e-02
Asian                                                                                            5.654e-02
Black                                                                                           -5.523e-02
Native_Hawaiian_or_P.Islander                                                                   -4.558e-02
loan_amount_000s                                                                                -4.012e-05
minority_population                                                                             -1.577e-03
                                                                                                Std. Error
(Intercept)                                                                                      6.616e-03
purchaser_type_nameCommercial bank, savings bank or savings association                          6.473e-03
purchaser_type_nameFannie Mae (FNMA)                                                             5.803e-03
purchaser_type_nameFarmer Mac (FAMC)                                                             1.876e-01
purchaser_type_nameFreddie Mac (FHLMC)                                                           5.959e-03
purchaser_type_nameGinnie Mae (GNMA)                                                             6.073e-03
purchaser_type_nameLife insurance company, credit union, mortgage bank, or finance company       6.250e-03
purchaser_type_nameLoan was not originated or was not sold in calendar year covered by register  5.553e-03
purchaser_type_nameOther type of purchaser                                                       6.971e-03
purchaser_type_namePrivate securitization                                                        1.401e-02
hud_median_family_income                                                                         4.286e-08
Hispanic_or_Latino                                                                               3.181e-03
Not_Hispanic_or_Latino                                                                           2.017e-03
American_Indian_or_Alaska_Native                                                                 1.015e-02
Asian                                                                                            2.813e-03
Black                                                                                            3.007e-03
Native_Hawaiian_or_P.Islander                                                                    1.245e-02
loan_amount_000s                                                                                 3.907e-06
minority_population                                                                              2.895e-05
                                                                                                t value
(Intercept)                                                                                     122.256
purchaser_type_nameCommercial bank, savings bank or savings association                          20.646
purchaser_type_nameFannie Mae (FNMA)                                                             -7.305
purchaser_type_nameFarmer Mac (FAMC)                                                              0.548
purchaser_type_nameFreddie Mac (FHLMC)                                                           -7.510
purchaser_type_nameGinnie Mae (GNMA)                                                            -11.729
purchaser_type_nameLife insurance company, credit union, mortgage bank, or finance company       20.425
purchaser_type_nameLoan was not originated or was not sold in calendar year covered by register -86.284
purchaser_type_nameOther type of purchaser                                                       15.649
purchaser_type_namePrivate securitization                                                         3.298
hud_median_family_income                                                                        -29.266
Hispanic_or_Latino                                                                               54.057
Not_Hispanic_or_Latino                                                                          111.131
American_Indian_or_Alaska_Native                                                                 -5.449
Asian                                                                                            20.101
Black                                                                                           -18.364
Native_Hawaiian_or_P.Islander                                                                    -3.661
loan_amount_000s                                                                                -10.268
minority_population                                                                             -54.480
                                                                                                Pr(>|t|)
(Intercept)                                                                                      < 2e-16
purchaser_type_nameCommercial bank, savings bank or savings association                          < 2e-16
purchaser_type_nameFannie Mae (FNMA)                                                            2.79e-13
purchaser_type_nameFarmer Mac (FAMC)                                                            0.583475
purchaser_type_nameFreddie Mac (FHLMC)                                                          5.94e-14
purchaser_type_nameGinnie Mae (GNMA)                                                             < 2e-16
purchaser_type_nameLife insurance company, credit union, mortgage bank, or finance company       < 2e-16
purchaser_type_nameLoan was not originated or was not sold in calendar year covered by register  < 2e-16
purchaser_type_nameOther type of purchaser                                                       < 2e-16
purchaser_type_namePrivate securitization                                                       0.000975
hud_median_family_income                                                                         < 2e-16
Hispanic_or_Latino                                                                               < 2e-16
Not_Hispanic_or_Latino                                                                           < 2e-16
American_Indian_or_Alaska_Native                                                                5.07e-08
Asian                                                                                            < 2e-16
Black                                                                                            < 2e-16
Native_Hawaiian_or_P.Islander                                                                   0.000252
loan_amount_000s                                                                                 < 2e-16
minority_population                                                                              < 2e-16
                                                                                                   
(Intercept)                                                                                     ***
purchaser_type_nameCommercial bank, savings bank or savings association                         ***
purchaser_type_nameFannie Mae (FNMA)                                                            ***
purchaser_type_nameFarmer Mac (FAMC)                                                               
purchaser_type_nameFreddie Mac (FHLMC)                                                          ***
purchaser_type_nameGinnie Mae (GNMA)                                                            ***
purchaser_type_nameLife insurance company, credit union, mortgage bank, or finance company      ***
purchaser_type_nameLoan was not originated or was not sold in calendar year covered by register ***
purchaser_type_nameOther type of purchaser                                                      ***
purchaser_type_namePrivate securitization                                                       ***
hud_median_family_income                                                                        ***
Hispanic_or_Latino                                                                              ***
Not_Hispanic_or_Latino                                                                          ***
American_Indian_or_Alaska_Native                                                                ***
Asian                                                                                           ***
Black                                                                                           ***
Native_Hawaiian_or_P.Islander                                                                   ***
loan_amount_000s                                                                                ***
minority_population                                                                             ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.4192 on 361666 degrees of freedom
Multiple R-squared:  0.2854,	Adjusted R-squared:  0.2854 
F-statistic:  8025 on 18 and 361666 DF,  p-value: < 2.2e-16


