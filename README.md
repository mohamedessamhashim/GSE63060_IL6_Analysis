# Analysis of Blood IL-6 Expression in Alzheimer's Disease using GSE63060
## Project Overview
This repository contains the data handling steps, SPSS analysis outputs, and a report detailing an investigation into the blood mRNA expression levels of the Interleukin-6 (IL-6) probe in individuals from the AddNeuroMed cohort (GSE63060). The analysis aimed to determine if IL-6 expression differs significantly between individuals diagnosed with Alzheimer's Disease (AD), Mild Cognitive Impairment (MCI), and healthy controls (CTL), while accounting for age, ethnicity and gender.
Research Question
Is the blood mRNA expression level of the IL-6 probe significantly different between diagnostic groups (AD, MCI, CTL) in the GSE63060 dataset, after controlling for age, ethnicity and gender?
## Data Source
The dataset GSE63060 (Batch 1 of the AddNeuroMed blood transcriptome data) was obtained from the NCBI Gene Expression Omnibus (GEO). The platform used was GPL10558.
- GSE63060 Series: [Link]https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63060
- GPL6947 Platform: [Link]https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL6947
## Repository Structure
* README.md: This file providing an overview of the project.
* report/: Contains the full analysis report in PDF format.
* data/: Contains the cleaned input data files used in the analysis pipeline.
    - GSE63060_Metadata_Cleaned.csv: Cleaned sample metadata.
    - GSE63060_Expression_RawMatrix.txt: The file containing only the transposed IL-6 probe expression data used for merging in SPSS. It’s the minimally cleaned original expression matrix with extracted IL-6 probe data.
    - GPL6947.annot: The platform annotation file used to identify the IL-6 Probe ID.
    - IL6_GSE63060_Dataset.sav: SPSS SAV file including the merged metadata and IL-6 probe expression data used to run the final results.
* spss_output/: Contains the raw output file generated by SPSS Statistics.
    - IL6_Results.spv: SPSS output file from the GLM analysis.
## Analysis Summary
This project focused specifically on analyzing the blood mRNA expression of the IL-6 probe with the ID ILMN_1699651 in the GSE63060 dataset.
The analysis pipeline involved:
1. Acquiring the GSE63060 dataset and GPL6947 platform annotation from GEO.
2. Cleaning and structuring sample metadata (Diagnosis, Age, Gender, Ethnicity) in Microsoft Excel.
3. Identifying the specific Probe ID for IL-6 using the platform annotation file.
4. Extracting the expression data for only the IL-6 probe from the full expression matrix in Excel.
5. Transposing the single-row IL-6 expression data in Excel to have samples as rows and IL-6 expression as a column.
6. Importing the cleaned metadata and the transposed IL-6 expression data into IBM SPSS Statistics v25.
7. Merging the metadata and IL-6 expression data in SPSS based on Sample ID.
8. Performing descriptive statistics on the merged dataset to characterize the sample and IL-6 expression levels.
9. Conducting a General Linear Model (GLM) - Univariate analysis in SPSS to test for significant differences in IL-6 expression between diagnostic groups (AD, MCI, CTL), including Age and Gender as covariates. Statistical significance was assessed at an alpha level of α=0.05.
## Requirements
* Microsoft Excel (for initial data handling)
* IBM SPSS Statistics 25 (or compatible version)
* Internet access (for data acquisition and literature review)
## Key Finding
The General Linear Model analysis revealed no statistically significant difference in blood IL-6 mRNA expression between the diagnostic groups (AD, MCI, CTL) in the GSE63060 dataset, after controlling for age and gender. The result for the main effect of Diagnosis was not significant (F (2, 312) = 0.136, p=0.873)
## Limitations
* Analysis is based on a single blood transcriptome dataset (GSE63060).
* Focus is limited to the mRNA expression level of a single probe for IL-6 on a specific platform (GPL6947).
* Blood expression may not directly reflect inflammatory processes or protein levels in the central nervous system.
## Conclusion
Based on this analysis, blood IL-6 mRNA expression, as measured in the GSE63060 dataset and controlled for age and gender, was not found to be a statistically significant marker differentiating AD, MCI, and control groups. This finding, while not statistically significant, contributes to the scientific record by indicating that blood IL-6 mRNA may not be a reliable diagnostic biomarker in this context and highlights the need for further investigation using alternative measurements (e.g., protein levels) or in independent cohorts.
## Contact
mohamedessamhashim
mohamedessamhashim@gmail.com
www.linkedin.com/in/mohamedessamha
License
[MIT License]
