# KPSS-Patent-Analysis
 Using API to JSON to generate a Document Term Matrix analyzing patent value


Data: 
The patent data is stored in KPSS_2022.zip, and the company data is stored in crsp_names.zip.  
Unzip the files and put in the same folder before running the program.  

This repository contains a replication and extension of the analysis performed in Kogan, Papanikolaou, Seru, and Stoffman (QJE 2017) (KPSS). The original study quantifies the value created by individual patents and shows that this measure positively predicts future firm growth. This project builds upon their work by exploring how specific features of patents, particularly those extracted from patent abstracts, correlate with patent value.   


Patent Value Data: Utilize the updated patent valuation data provided by KPSS, which covers the period from 1926 to 2022.   

Patent Grant Data: Patent grant details, including abstracts, are obtained from the USPTO Bulk Data API for patents granted in January 2019.

Company Names: Merge in company names using the "permno" field and the "crsp_names.csv" dataset.

Textual Analysis: Perform textual analysis on patent abstracts to generate a document-term matrix. Preprocessing and tokenization include:
- Lowercasing and selecting only alphabetic tokens.
- Including unigrams and bigrams.
- Requiring tokens to be at least 3 characters long.
- Excluding stop words.
- Restricting the matrix to the 1,000 most common words.

