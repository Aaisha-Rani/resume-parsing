# resume-parsing
A Python-based solution for extracting structured information from PDF resumes. This project leverages pdfplumber, regex, and custom logic to parse candidate data, classify college tiers, and prepare datasets for analysis and automation workflows.  

Automated Resume Parsing and Job Fit Prediction

🚀 Project Overview

This project is an end-to-end system that parses resumes in PDF format, extracts structured information, and matches candidate profiles against job descriptions using semantic similarity. The final output is a detailed Excel report ranking resumes based on how well they fit the job requirements.

🧰 Problem Solved

Recruiters often receive thousands of resumes per role. Manually screening them is time-consuming and error-prone. This system automates:

Resume parsing (education, experience, projects, etc.)

College tier classification (Tier 1/2/3)

Project extraction

Semantic job-resume matching

Outputting an Excel report with job-fit probability

🔧 Tech Stack

Python

pdfplumber or PyMuPDF for PDF parsing

fuzzywuzzy for fuzzy string matching

pandas for data processing

sentence-transformers (BERT) for semantic similarity

openpyxl for Excel export

💡 Key Features

Parses resumes from a folder of PDFs

Extracts key fields: Institute, Year, CGPA, Branch, Experience, Projects

Maps colleges to tiers using fuzzy matching

Uses BERT to compute job fit score

Exports all results to Excel

⚖️ Why These Tools Were Chosen

✅ PDF Parsing: pdfplumber

Chosen for accurate and lightweight extraction of text from PDFs. It works well for standard resume layouts.

✅ Fuzzy Matching: fuzzywuzzy

Used to robustly match institute names from resumes to those in the college tier dataset. This handles abbreviations, typos, and formatting inconsistencies.

✅ Semantic Matching: BERT via sentence-transformers

BERT was chosen because it captures the meaning of text, not just keywords. This allows for accurate matching between resumes and job descriptions, even when phrased differently.

✅ Why Not Traditional ML?

Machine learning models like Random Forest require large labeled datasets. Since we don't have resume/job outcome labels, a pre-trained model like BERT is more suitable and ready-to-use.

📊 Project Workflow

Extract text from PDF resumes

Parse fields using regex and string rules

Map institutes to tiers using fuzzy matching

Load job description from CSV

Use BERT to compute cosine similarity between resume and JD

Store similarity as Job_Fit_Probability (%)

Export to Excel with all extracted fields
