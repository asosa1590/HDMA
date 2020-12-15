
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
