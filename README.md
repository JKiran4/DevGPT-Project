# DevGPT dataset analysis

### Background
DevGPT is a comprehensive dataset of 17,913 ChatGPT prompts and answers which are grouped into several software development artifacts (commits, issues, discussions, files, pull requests, and hacker news sharings). All data was retrieved from the DevGPT repository: https://github.com/NAIST-SE/DevGPT. The files in the repository are also split into folders corresponding to different snapshots in time and are in a json format. Our goal in this project is to join these files together to explore three research questions related to the converstaions with ChatGPT:

RQ1. What types of issues (bugs, feature requests, theoretical questions, etc.) do developers most commonly present to ChatGPT?
RQ2. How do the answers provided by ChatGPT vary between models (length, content, tone, etc.)?
RQ3. Can we reliably predict the author of a given piece of text from the content of the message?

### Methodology
Our methodology varies slightly for each research question, specifically with the data we used. For RQ1 and RQ2 we use 'snapshot_20231012', as they are primarily focused on exploration of the data as opposed to building a machine learning model. For RQ3, we use the entire dataset to gather information from as many authors as possible for classification. For all of these questions, we join the software development artifacts files into a single master file, ensuring we extract relevant columns that are nested within the json structure. Note that for all questions, we download each of the json files from the snapshots into a local folder. Afterwards, we run our jupyter notebooks in the same folder location as the json files. Also note that some of the code from RQ2 is also used for RQ1, so there will be similarities apart from exploration of the research questions themselves.

### Required libraries
To run the code in this repository, please ensure the following libraries are installed to your python environment: 
- os
- pandas
- json
- altair
- langdetect
- re
- matplotlib
- seaborn
- gensim
- numpy
- sklearn
