# CSE6324Team5
# Domain based clustering of SIMULINK dataset.
Searching for projects or code on web is the most common activity we perform as students. 
When facing a problem, we go to google and type in the keywords we want to search for, incase if we want to look for any previously implemented projects, we try finding it on GitHub.
Currently Search on GitHub works on finding all relevant projects based on the matching the search keyword.
We want to improve this standard search by clustering the projects together based on their domain or category they belong to. 
The user will enter the domain he/she is interested in, and our system will try to group together similar projects based on the domain specified by the user.
We will explore on how GitHub search works currently, what clustering algorithms we can use to maximize/optimize our search result.

# Goal: 
The aim of the project is to group software projects based on the category of the projects
# Input: 
The dataset of simulink project provided by sohil.
# Technology Used: 
Python
# Process Overview
1.The first step for us would be explore the SIMULINK dataset
2.Identify features that we can use from the dataset for clustering
3.Pre-processing the dataset, feature extraction and generating a csv file to be used for feeding as input to the model
4.Building a model for clustering the projects based on the features that we identified in step 2. In this step we would analyze various clustering algorithms that could be 5.used and comparing their results and finalizing the one with the best results.
6.Evaluating the model with training and testing dataset.
7.Obtaining the final grouped/clustered projects
# Iteration 1 Activities: Feature Extraction and Data Pre-Processing
Step 1: Observed all the tables in the given repository to identify which features woyuld be best suited for our clustering approach
Step 2: Decided on using Summary and Category as important features to idenitfy the grouping based on the category of the project.
Step 3: Applying PreProcessing on "Summary" coloumn.The Summary coloumn contains the summary of the projects that we have, and category contains the category the project belongs to. Since the values in these coloumn are not numerical but categorical or textual, we would have to perform text preprocessing in order to begin with feature extraction.
Step 4: We used the text preprocessing for Natural launguage to convert the sentences in the "Summary" coloumn to a format that is understandable by the machine.
Step 4.a) Tokenization: The process of converting Sentences to tokens.
Step 4.b) Filtering Tokens: Removing Tokens which contain numerical values or does not conatin any textual value.
Step 4.c) Stemming: Bringing down a word from its various forms to its root word. This Process allows us to establish meaning to different forms of the same words without having to deal with each form separately. 
Step 5: TFIDF Vectorization: In this step we create a TFIDF vector matrix for the "Summary" column. This process converts the words obtained after performing step 4 on "Summary" column,into numerical values so that we can apply clustering algorithm on pre-processed data.
