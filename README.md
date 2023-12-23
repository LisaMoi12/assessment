# Proteomics Calculator

## Content

1. [Introduction](#introduction)
2. [Step 1: Installation and Preparing Excel Files](#step-1-installation-and-preparing-excel-files)
3. [Step 2: Filtering Data and Calculating Ribosomal Average](#step-2-filtering-data-and-calculating-ribosomal-average)
4. [Step 3: Final Calculations of Protein Concentrations](#step-3-final-calculations-of-protein-concentrations)
5. [Usage](#usage)
6. [Example](#example)



## Introduction

The Proteomics Calculator is designed to analyze Excel files containing results from LCMS analysis of bacterial samples conducted in proteomics facilities. Its purpose is to simplify and automate the final proteomics analysis process, eliminating the need for researchers to make repetitive steps for each Excel spreadsheet with proteomics results.

## Step 1: Installation and Preparing Excel Files

To analyze Excel spreadsheets, this code uses the pandas library (`import pandas as pd`). 

The next step is to import the data: (`data = pd.read_excel('insert file pathway')`), provided file named "TEST" can be used to run this code. 
The structure of each Excel spreadsheet follows a specific format, containing various columns. For our research, we focus on specific columns: 'Accession', 'Description', '# Peptides', and 'Area'. 

Rows with less than 3 in the 'Peptides' column are disregarded as the value is too small. Sorting the data by the 'Peptides' column and removing rows with values less than 3 is the initial step.

## Step 2: Filtering Data and Calculating Ribosomal Average

The next step involves sorting the data and moving all hits with ribosomal units of E. coli to the top of the spreadsheet. Due to the variability in ribosomal unit naming conventions, the code employs various filters to account for different ribosomal units. Subsequently, the code calculates the ribosomal average, a key value for subsequent calculations.

## Step 3: Final Calculations of Protein Concentrations

The final step computes the protein concentrations. The values in the 'Area' column are divided by the previously calculated 'Ribosomal average'. In this research, the focus is on determining the content of the target protein 'blaTEM' with the accession 'A0A0X9U5K8'.

The code provides output with the calculated value representing the content of the target protein in the sample.

## Usage 

It can be run in the Jupiter Notebook as the easiest way, or you can retrieve this code and run it in the terminal. 

## Example 

This code is very specific and can be used for LCMS analysis output only, or changed and adjusted to analyse other spreadsheets. 

### Step 1.
Importing data and initial formatting.
<img width="1164" alt="Screenshot 2023-12-22 at 19 00 32" src="https://github.com/LisaMoi12/assessment/assets/153204813/1ffc0fcb-0f8c-4c91-b34a-5a6a8bc09eed">

### Step 2.
Filtering Data.
<img width="1170" alt="Screenshot 2023-12-22 at 19 13 20" src="https://github.com/LisaMoi12/assessment/assets/153204813/5ca1c3b5-3ba2-47ba-abe0-46f2b085f91c">
Calculating 'Ribosomal Average'
<img width="1175" alt="Screenshot 2023-12-22 at 19 53 23" src="https://github.com/LisaMoi12/assessment/assets/153204813/77e516cd-bffc-4ec6-9c7a-5c8517775146">
<img width="1167" alt="Screenshot 2023-12-22 at 19 48 36" src="https://github.com/LisaMoi12/assessment/assets/153204813/6c8f5d82-145a-471c-b3d4-7f65ac557359">

### Step 3.
Final calculations of protein concentrations.
As a result of the final lines of code, we have output value of the concentration of the target protein.
<img width="1172" alt="Screenshot 2023-12-22 at 20 05 05" src="https://github.com/LisaMoi12/assessment/assets/153204813/c2ad5ceb-82b6-4cc7-abfb-b0e8916ec650">
