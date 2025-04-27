# antidepressants_analysis - data guidelines

Analysis of adverse events of antidepressants based on FAERS


The dataset is too large to upload to GitHub. Please find it here for re-run (not recommended): https://drive.google.com/drive/folders/1DmMZ-rO1vcvWYchGKfkNGqIUqdi_sD6a?usp=sharing

* raw_data: include data from FAERS Q1 2018 to Q4 2019 (format name for coding) and MedDRA data 27.1 ~ 1.67 GB
* cleaned_data_by_step - refer to notebook ~ 32.6 MB
* check_map_data (same as the file in GitHub): manual data check and map - refer to the notebook ~ 1.7 MB.

Note for rerunning the notebooks:

* Steps 1, 2, 3, 4, 6, 7: Can run on the local server (Macbook Pro, M1 chip, Memory 16 GB, no GPU).
* Step 5: The author ran on the local server, which took 5 hours to complete. If you would want to re-run, I recommend using this link for Google Colab, too, but I haven't checked the reproducibility (https://drive.google.com/file/d/1_b1R6Ij7QFeFIIg1aH7XNni_prtVxpEW/view?usp=sharing).
