
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
