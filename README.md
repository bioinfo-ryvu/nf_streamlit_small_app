# nf_streamlit_small_app

## Nextflow usage and modification

### Clone: https://nf-co.re/differentialabundance/1.5.0/docs/usage
You will run differentialabundance pipeline with profile **test_full**

#### Hint: This profile has a small error in his config, so you need to fix based on this repo alteration:
https://github.com/nf-core/test-datasets/tree/differentialabundance

After being able to run, we want you to add these modifications in workflow, **NOT output files**:
1) Add a cutoff of FDR < 0.25 to GSEA-part of the report; Merge UP and DOWN tables;
2) Also add a cut off padj < 0.05 and |FC| > 1.3 to differentially expressed genes; Merge UP and DOWN tables; Add a new column to tag comparison.

#### Hint: Modifications will be done in Rmarkdown file inside pipeline.

## Dockerized Streamlit app
As input, you will add:
1) **GSEA files: <PATH-TO-RESULTS>/report/gsea/*/*gsea_report_for_*.tsv
2) **DESeq2 files: <PATH-TO-RESULTS>/tables/differential/*deseq2.results.tsv
3) Annotation: <PATH-TO-RESULTS>/tables/annotation/**.tsv

### Using streamlit, run an app capable of:
1)	Run an interactive volcano plot with output from DESeq2;
2)	Run a dot plot with output from GSEA;
3)	We should always be able to see gene SYMBOLS, not gene ids, i.e Brca1, not ENSMUSG00000017146.
4)	Make sure to include the most essential information from DESeq2 and GSEA, i.e. FDR, FC, NES, etc.
5)	This tool needs to be run from a docker container;
6)	Nice to have: Multiple results from GSEA + DESeq2 will be stored in two different folders, app could access than and list options.
 
## Details
1.	Feel free to use any LLM in your work as ChatGPT / DeepSeek / Gemini.
2.	Document your developing process. Update README.md!
3.	Make it sure your application is organized and runnable. DESCRIBE how it should be used.
4.	We are NOT looking for speed coders, so feel free to manage your time way you want. Delivery in 6 hour or 5 days will not give you any advantage.
5.	In case you need any orientation please send a message to bioinfo@ryvu.com, we will do our best to answer any questions.
