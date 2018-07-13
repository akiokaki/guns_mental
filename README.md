## Are shootings caused by inadequate mental institutions?
This analysis aims to understand the relationship between mental institution of a community to the occurance of gun casualties. Specifically,

1.	Is there a correlation between gun deaths (homicide) and the comprehensiveness of mental treatment services each institution offers among different States?
2.	Is there a correlation between gun deaths (homicide) and the average number of rehabilitation services each institution offers among different States?
3.	Is there a correlation between gun deaths (homicide) and the availability of a crisis intervention among different States?
4.	Is there a correlation between gun deaths (homicide) and the average number of payment reduction program offered among different States?


Detailed report can be found under "project_report.pdf". Analysis was done on jupyter notebook.

Gun deaths data was retrieved from the CDC at https://wonder.cdc.gov/controller/datarequest/D77, and mental institution data from https://datafiles.samhsa.gov/study-dataset/national-mental-health-services-survey-2015-n-mhss-2015-ds0001-nid17098.

---
Workflow:
1. Clean up data and Format

   - Cleaned up CDC data by getting rid of the non-data related sections using a RegEx split
   - Read respective files into pandas dataframes for analysis
   - Filtered useless responses (i.e. missing data)
   - Created function using the 'us' library to convert State abbreviations to full names
   - Merged the datasets on State names
   
2. Analyze

   - Created aggregate values for average number of treatments available, and rehab programs
   - Checked normality of variables using a QQ plot
   - Normalized gun deaths by log transformation
   - Ran correlations
   
3. Vizualize
   - Drew scatterplot with marginal histograms
   
 ---
 
 Conclusions:
- While mental health treatment and gun homicides show a clear negative correlation to each other, gun homicides and rehabilitation services, and, to an extent, crisis intervention services offer a murkier interpretation 
- Payment reduction program seems to be completely unrelated to gun deaths. 
