# AI Usage Final Project Bioinformatics

### Code Block 1

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to double-check that the Python libraries I used from the Module 8 assignment were correct.
3. **Snippet of prompt(s):** “Are these Python libraries correct to work with gene expression datasets and perform feature selection?"
4. **What I changed before committing:** I used the provided import statements without making any major changes.
5. **How I verified correctness (tests, sample data):** I ran the cell in Google Colab and confirmed the libraries imported without errors and the success message appeared.

### Code Block 2

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to generate code to download the GSE36761 and GSE217772 gene expression files directly from NCBI GEO.
3. **Snippet of prompt(s):** "Can you write Python code to download the gene expression files for GSE36761 and GSE217772 directly into Google Colab so I don't have to upload them manually?"
4. **What I changed before committing:** I used the provided code.
5. **How I verified correctness (tests, sample data):** I ran the download code and confirmed that both files were retrieved and saved as compressed text files, with a confirmation message indicating the downloads completed.

### Code Block 3

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me inspect the structure of both datasets before beginning preprocessing.
3. **Snippet of prompt(s):** "Now that I have both datasets downloaded, how can I look at their dimensions, column names, and first few rows to see how they're organized?"
4. **What I changed before committing:** I kept the code mostly unchanged.
5. **How I verified correctness (tests, sample data):** I examined the printed dataset dimensions, column names, and the first five rows of each dataset to identify the gene identifier columns and sample expression values.

### Code Block 4

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to write code to standardize gene identifiers between the two datasets, remove duplicate genes, and keep only genes present in both datasets.
3. **Snippet of prompt(s):** "The two datasets don't have exactly the same gene ID format. Can you help me remove the Ensembl version numbers, get rid of duplicate genes, and find which genes they have in common?"
4. **What I changed before committing:** I used the generated code with minimal changes.
5. **How I verified correctness (tests, sample data):** I checked the number of genes in each dataset and confirmed that the matching step identified 16,385 shared genes. I also examined the resulting training and testing matrix dimensions.

### Code Block 5

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me display all the training sample names so I could identify the TOF samples and the appropriate control samples.
3. **Snippet of prompt(s):** "Can you give me a simple piece of code that prints out all the sample names in my training dataset? I need to figure out which ones are the controls."
4. **What I changed before committing:** I used the code without major changes.
5. **How I verified correctness (tests, sample data):** I reviewed the printed sample names and identified the samples labeled with TOF- and NH- prefixes.

### Code Block 6

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me select the TOF samples and four right ventricular control samples for the training dataset.
3. **Snippet of prompt(s):** "I only want to use the four right ventricular controls, NH-02, NH-04, NH-06, and NH-08, along with all the TOF samples. Can you write code to filter the training dataset to just those samples?
4. **What I changed before committing:** I used the code with very few changes.
5. **How I verified correctness (tests, sample data):** I checked the output to confirm that the filtered training dataset contained 22 TOF samples and four controls, for a total of 26 samples.

### Code Block 7

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to generate code to remove genes with very low expression levels before performing feature selection.
3. **Snippet of prompt(s):** "How can I filter out genes that have really low expression? I want to keep genes with expression greater than 1 in at least 20% of the training samples and then keep those same genes in the testing dataset."
4. **What I changed before committing:** I used the generated filtering code without making substantial changes.
5. **How I verified correctness (tests, sample data):** I compared the number of genes before and after filtering. The number decreased from 16,385 to 14,985, and I checked that the training and testing datasets retained the same genes.

### Code Block 8

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me visualize the gene expression distributions in both datasets using log-transformed values and boxplots.
3. **Snippet of prompt(s):** "Can you help me make boxplots of the gene expression values for both datasets after a log2 transformation? I also want to save the figure so I can use it in my report."
4. **What I changed before committing:** I kept most of the provided code.
5. **How I verified correctness (tests, sample data):** I ran the code and examined the two boxplots to compare the expression distributions between the training and testing datasets. I also checked that the figure was generated and saved as a PNG file.

### Code Block 9

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to generate code to summarize expression values in both datasets.
3. **Snippet of prompt(s):** "Can you write code to show the mean, standard deviation, minimum, maximum, and quartiles for the log-transformed expression values in both datasets?"
4. **What I changed before committing:** I used the code without substantial modifications.
5. **How I verified correctness (tests, sample data):** I examined the summary tables for both datasets and confirmed they included the requested descriptive statistics.

### Code Block 10

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me examine the total RNA-seq counts for each testing sample to see whether the samples had different sequencing depths.
3. **Snippet of prompt(s):** "How do I calculate the total read counts for each sample in my testing dataset? I want to see if some samples have a lot more counts than others."
4. **What I changed before committing:** I used the provided code with minimal changes.
5. **How I verified correctness (tests, sample data):** I reviewed the total counts calculated for each testing sample and the ratio between the highest and lowest sample totals.

### Code Block 11

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to generate code to normalize the raw RNA-seq counts in GSE217772 using counts per million (CPM) and then log-transform the normalized values.
3. **Snippet of prompt(s):** "My testing dataset has raw RNA-seq counts, but my training dataset already has normalized expression values. Can you help me normalize the testing data using counts per million and then apply a log2 transformation?"
4. **What I changed before committing:** I used most of the generated code without major changes.
5. **How I verified correctness (tests, sample data):** I checked the dimensions of the normalized testing dataset and examined the median log2 CPM values for each sample. I also confirmed that the testing dataset retained the genes selected during training preprocessing.

### Code Block 12

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me compare average gene expression between the two datasets using a Spearman correlation and a scatterplot.
3. **Snippet of prompt(s):** "How can I check whether the average gene expression patterns are similar between my training and testing datasets? Can you calculate a Spearman correlation and make a scatterplot?"
4. **What I changed before committing:** I used the code with very few modifications.
5. **How I verified correctness (tests, sample data):** I examined the calculated Spearman correlation coefficient, its p-value, and the scatterplot comparing average gene expression between the two datasets. I also checked that the plot was saved successfully.

### Code Block 13

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me select the 20 genes showing the biggest statistical differences between TOF and control samples using ANOVA F-scores.
3. **Snippet of prompt(s):** "Now I want to start feature selection. Can you help me use ANOVA F-scores to find the top 20 genes that are most associated with TOF versus the controls and save the results as a CSV?"
4. **What I changed before committing:** I used most of the generated code with minimal changes.
5. **How I verified correctness (tests, sample data):** I checked that the code produced a table with 20 selected genes, their Ensembl IDs, F-scores, and p-values. I also checked that the results were exported to a CSV file.

### Code Block 14

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me determine whether the top selected genes had higher or lower average expression in TOF samples compared with controls.
3. **Snippet of prompt(s):** "For the top 20 genes, can you help me calculate the average expression in the TOF and control groups and show whether each gene has higher or lower expression in TOF?"
4. **What I changed before committing:** I used the provided code with minimal changes.
5. **How I verified correctness (tests, sample data):** I reviewed the updated table containing the control means, TOF means, log2 expression differences, and expression direction. I checked that the table was generated and exported successfully.

### Code Block 15

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me match GWAS-associated candidate genes to the Ensembl gene identifiers in my expression dataset.
3. **Snippet of prompt(s):** "I want to use GPC5 as a candidate gene from the TOF GWAS research, but my dataset uses Ensembl IDs instead of gene symbols. Can you help me use MyGene.info to map the IDs and see whether GPC5 is in my filtered dataset?"
4. **What I changed before committing:** I used most of the generated code.
5. **How I verified correctness (tests, sample data):** I reviewed the gene-mapping results and checked the number of GWAS candidate genes found in the filtered expression dataset. I also checked that the selected gene table was exported.

### Code Block 16

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me figure out why GPC5 wasn't appearing in the GWAS-informed feature selection results.
3. **Snippet of prompt(s):** "GPC5 isn't showing up in my selected genes. Can you help me check its Ensembl ID and see whether it was actually mapped correctly?"
4. **What I changed before committing:** I used the troubleshooting code without making major modifications.
5. **How I verified correctness (tests, sample data):** I checked the MyGene.info query result for GPC5, the number of genes successfully mapped to symbols, and the gene mapping table for any GPC5 matches.

### Code Block 17

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me determine whether GPC5 was present in the original datasets and whether it had been removed during gene matching or low-expression filtering.
3. **Snippet of prompt(s):** "Can you write code to check if GPC5 was in the original training and testing datasets and whether it got removed when we filtered the genes?"
4. **What I changed before committing:** I kept the code mostly unchanged.
5. **How I verified correctness (tests, sample data):** I checked whether the GPC5 Ensembl ID was present in the original training data, matched training data, filtered training data, and testing data. This helped determine which preprocessing stage excluded the gene.

### Code Block 18

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me expand the GWAS-informed feature selection to include GPC5, PTPN11, and NRP1 and determine which genes were available after preprocessing.
3. **Snippet of prompt(s):** "Can we check GPC5, PTPN11, and NRP1 together instead of just GPC5? I want a table showing which genes are in the original datasets and which ones passed the expression filter."
4. **What I changed before committing:** I used the generated code with minimal changes.
5. **How I verified correctness (tests, sample data):** I reviewed the GWAS candidate table and checked whether each gene was available in the original training data, original testing data, and filtered expression data. The final retained candidates were PTPN11 and NRP1.

### Code Block 19

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to help me finalize the expression-based and GWAS-informed feature selection using the filtered datasets and export the selected genes and expression matrices for the next stage of the project.
3. **Snippet of prompt(s):** "Now that we've filtered the datasets and identified the GWAS genes, can you help me redo the top 20 gene selection using the filtered training data and save separate training and testing CSV files for the expression-based and GWAS-based genes?"
4. **What I changed before committing:** I used most of the generated code as provided, without making substantial changes.
5. **How I verified correctness (tests, sample data):** I checked that the code selected 20 expression-based genes and retained the available GWAS candidates. I reviewed the dimensions of the exported training and testing matrices, checked the updated top 20 gene table, and confirmed that the six CSV output files were generated for the next stage of the analysis.

### Code Block 20

1. **Tool/model & version:** Claude (Anthropic): Claude Sonnet 5.5 and Claude Opus 5.5
2. **What I asked for:** I asked Claude to help me build and evaluate Logistic Regression and Random Forest models in scikit-learn using our preprocessed data.
3. **Snippet of prompt(s):** "Let's work on a machine learning model utilizing this data in Google Colab."
4. **What I changed before committing:** I used the generated code as Step 13, and changed the model-selection line to break ties using balanced accuracy before running the final test.
5. **How I verified correctness (tests, sample data):** I checked that the training and test sets had the expected sample counts, that the always-TOF baseline behaved as expected, and that I evaluated the test set only once.

### Code Block 21

1. **Tool/model & version:** Claude (Anthropic): Claude Sonnet 5.5 and Claude Opus 5.5
2. **What I asked for:** I asked Claude to help me understand why every test sample was predicted as TOF.
3. **Snippet of prompt(s):** "Why did all three models classify every test sample as TOF?"
4. **What I changed before committing:** I used the code without major changes and labeled it as post-hoc so it does not change the test result.
5. **How I verified correctness (tests, sample data):** I ran the cell and confirmed the output matched the test results.

### Code Block 22

1. **Tool/model & version:** Claude (Anthropic): Claude Sonnet 5.5 and Claude Opus 5.5
2. **What I asked for:** I asked Claude how to find the package versions used in our notebook.
3. **Snippet of prompt(s):** "How do I get the versions for the software?"
4. **What I changed before committing:** I installed mygene in the same session so I could print its version.
5. **How I verified correctness (tests, sample data):** I compared the printed versions with the Methods section and environment.yml.

### Code Block 23

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to simplify and reorganize my code
3. **Snippet of prompt(s):** “How do I simplify the code that will prepare my data and identify the GWAS- *my own code*”
4. **What I changed before committing:** I used my code for the first part of the section (imports and the “from sklearn” code); however, I changed the data preparation and GWAS identification to simpler code provided by ChatGPT.
5. **How I verified correctness (tests, sample data):** I ran the cell to check its similarities to the rest of the team's code.

### Code Block 24

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to give me a baseline code for cross-validation that will select only k values
3. **Snippet of prompt(s):** “How do I code cross-validation that will select k values”
4. **What I changed before committing:** I used my code from the last part of the section to define the machine learning models and added what ChatGPT gave me before my coding section.
5. **How I verified correctness (tests, sample data):** I ran the cell, confirmed the output matched the test results, and checked for errors in the code.

### Code Block 25

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT to give me a baseline code for defining the strategy before comparing or starting the expirement/ testing
3. **Snippet of prompt(s):** “How do I create a baseline code for defining the strategy before comparing”
4. **What I changed before committing:** I had no code of my own because I didn't know what to do.
5. **How I verified correctness (tests, sample data):** I ran the cell, confirmed the output matched the test results, and checked for errors in the code.

### Code Block 26

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT when to use a pipeline when training different systems so missing-value handling and scaling are learned within each training fold.
3. **Snippet of prompt(s):** “Based on my code, I need a pipeline in order to handle missing values and learn within each training fold ”
4. **What I changed before committing:** I had a baseline of what to label my table in my independent table; however, the rest was made by ChatGPT in order to have cleaner code and a cleaner result
5. **How I verified correctness (tests, sample data):** I ran the cell, confirmed the output matched the test results from the past tables, and checked for a simpler results table.

### Code Block 27

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT how to make a confusion table.
3. **Snippet of prompt(s):** “Based on my past data, how to make a confusion matrix”
4. **What I changed before committing:** I had a baseline of the code  to display the results and visualization; however, the ChatGPT code was all in use for making the confusion matrix
5. **How I verified correctness (tests, sample data):** I ran the cell, confirmed the output matched the test results from the block 25 table to see if there was a relation, and inferred that the results showed worse performance or no improvement in GWAS.

### Code Block 28

1. **Tool/model & version:** ChatGPT
2. **What I asked for:** I asked ChatGPT how to make sure my GWAS conclusion was correct.
3. **Snippet of prompt(s):** “Based on my past data, how code where I could only see GWAS improvements”
4. **What I changed before committing:** I had a baseline of the code I wanted to see, but the rest of the code is finding the test results and the different scores of GWAS
5. **How I verified correctness (tests, sample data):** I ran the cell, confirmed the output matched the test results from the block 25 table to see if there was a relation, and inferred that the results showed worse performance or no improvement in GWAS.

### Code Block 29

6. **Tool/model & version:** ChatGPT
7. **What I asked for:** I asked ChatGPT how to make a PCA plot to find the differences between TOF and the control.
8. **Snippet of prompt(s):** “Based on my past data, how do I code a PCA plot”
9. **What I changed before committing:** I had a baseline of the genes I wanted to see, but the rest of the code is to define a simple PCA plot
10. **How I verified correctness (tests, sample data):** I ran the cell and confirmed the output matched the test results in relation to the rest of the results.
