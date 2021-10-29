# Generate Suicidality Data
* SI/SA_total_objects_for_all_mri.ipynb
  * concatenate all the children clinical data who have structural MRI or diffusion MRI or resting-state fMRI or 3 tasks fMRI data         
  * select clinical outcome columns
  * remove duplicated subjects information in terms of subject
   outcome: SI/SA_total_clinical.csv  
   
* Suicidality_making_control.ipynb
  * make new column whose name is "Health_control". It means whether subjects don't have any mental disorders.
  * healty can be measured by ksad & CBCL total Prob score (all ksads = 0, ToProb.CBCL <= 65)
  * output: control_subjects.csv
  
* Suicidality_clinical_outcome.ipynb
  * common subjects information between demo.total.csv file and data that I made
  * input: SI/SA_total_clinical.csv, control_subjects.csv
  * output: SI_SA_4_columns_and_clinical_outcome.csv
