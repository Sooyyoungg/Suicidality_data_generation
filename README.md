# Generate Suicidality Data with phenotype & clinical outcomes
## Code
* SI/SA_total_objects_for_all_mri.ipynb
  * concatenate all the children clinical data who have structural MRI or diffusion MRI or resting-state fMRI or 3 tasks fMRI data         
  * select clinical outcome columns
  * remove duplicated subjects information in terms of subject
  * input: MRI table data
  * output: SI/SA_total_clinical.csv  
   
* Suicidality_making_control.ipynb
  * make new column whose name is "Health_control". It means whether subjects don't have any mental disorders.
  * healty can be measured by ksad & CBCL total Probability score (all ksads = 0, ToProb.CBCL <= 65)
  * input: ABCD_phenotype_total - ABCD_phenotype_total.csv (containing ksad & CBCL information)
  * output: control_subjects.csv
  
* Suicidality_clinical_outcome.ipynb
  * concatenate Suicidalideation column and SuicideAttempt column into one dataframe.
  * make Suicide_Control column and fill the values whether Suicidalideation and SuicideAttempt vales are 0.
  * make Health_control column and fill the values using control_subjects.csv file values.
  * input: SI/SA_total_clinical.csv, control_subjects.csv
  * output: SI_SA_4_columns_and_clinical_outcome.csv

* Suicidality_data_total_clinical+demo+covariate+intelligence.ipynb
  * fine common subjects information between demo.total.csv file and data that I made
  * merge ABCD total phenotype columns(demo.total.csv) and clinical outcome columns.
  * input: demo.total.csv, SI_SA_4_columns_and_clinical_outcome.csv
  * output: Suicidality_data_final2.csv

## Data
* structural data : data_si_unppc_sMRI_train.csv + data_si_unppc_sMRI_test.csv
* diffusion data : data_si_unppc_dMRI_train.csv + data_si_unppc_dMRI_test.csv
* resting state functional data : si_ppc_rsfMRI_train.csv + si_ppc_rsfMRI_test.csv
* N-back data : si_ppc_nbackfMRI_train.csv + si_ppc_nbackfMRI_test.csv
* Stop Signal Task data : si_ppc_sstfMRI_train.csv + si_ppc_sstfMRI_test.csv
* Mid data : si_ppc_midfMRI_train.csv + si_ppc_midfMRI_test.csv
