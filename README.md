# DATA 542 Final Project, DevGPT dataset analysis

#### Background
DevGPT is a comprehensive dataset of 17,913 ChatGPT prompts and answers which are grouped into several software development artifacts (commits, issues, discussions, files, pull requests, and hacker news sharings). All data was retrieved from the DevGPT repository: https://github.com/NAIST-SE/DevGPT. The files in the repository are also split into folders corresponding to different snapshots in time and are in a json format. Our goal in this project is to join these files together to explore three research questions related to the converstaions with ChatGPT:

1. H
2. h
3. H

#### Methodology
For each questions, we follow a similar methodology in processing the files. We first get a list of file paths from the DevGPT repository, normalize columns to extract out all of the data from each file and join the files together into a single master file, called preprocessing.ipynb. For each question, we create a separate workbook, corresponding to RQ_X.ipynb in the repository. Our final report containing all of our experiments and results can be found in final_report.pdf

# Required libraries
To run the code in this repository, please ensure the following libraries are installed to your python environment: 
- os
- pandas
- json
- altair
- langdetect
- re
- matplotlib
- seaborn
