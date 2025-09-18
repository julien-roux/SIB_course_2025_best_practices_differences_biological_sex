# SIB course: Best Practices for Investigating Gene Expression Differences by Biological Sex -- Hands-on session

October 27th, 2025

## Motivation

The past decades have seen large calls for consideration of the sex dimension into research and clinical projects. However as we progress towards more frequent inclusion of this variable, the design of experiments evolved to be much more complex, [in particular challenging the analysis steps](https://www.cell.com/cell/fulltext/S0092-8674(24)00174-0).
This hands-on tutorial is designed to foster a critical perspective on integrating the sex dimension in bioinformatic analyses. Through a practical exercise focusing on Differential Expression (DE) analysis, we will revisit the conclusions from a published study in light of the results of our re-analysis. 
We aim at rigourously testing for sex differences and notably for the presence of interactions between experimental factors. Following on Frédéric's presentation, we would like to use this hands-on to draw your attention at power issues potentially affecting conclusions, and how to best report results of your analyses.

## Dataset 
Today's dataset is described in this paper ["Tamoxifen induction of Cre recombinase does not cause long-lasting or sexually divergent responses in the CNS epigenome or transcriptome: implications for the design of aging studies"](https://link.springer.com/article/10.1007/s11357-019-00090-2), and focuses on the potential side effects of Tamoxifen treatment, widely used to induce CreERT2 activity in transgenic mouse systems. Tamoxifen acts as an antagonist of estrogen receptor (ER), which could cause differences in response across sexes.

![](img/Screenshot%202024-06-17%20at%2014.55.37.png)

Raw and processed data are available from GEO [(accession GSE135752)](GEO:%20https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE135752)

## Organization of the `hands-on` folder

 This folder gathers the the `.qmd` scripts used to guide the hands-on session. 
 
- The dataset from this paper was obtained from the [recount3 project](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-021-02533-6), reprocessing uniformly thousands of bulk RNA-seq datasets available from public repositories (8,679 human and 10,088 mouse studies so far). 
See the ![](dataset_retrieval_recount3.qmd) script where we end up saving the dataset in a `RangedSummarizedExperiment` object.
 
- The differential expression analysis will be conducted with classical Bioconductor packages ![limma](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2014-15-2-r29) or ![DESeq2](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-014-0550-8). The respective `.qmd` scripts are ![](hands_on_limma.qmd) and ![](hands_on_DESeq2.qmd) and you can choose the option you feel more comfortable with.
- A slightly more complex way of analyzing the dataset, maybe more powerful, is shown in ![](hands_on_limma_advanced.qmd). Use it if you are already familiar with DE analysis with the limma packages

## Installation
It is recommended to have an up-to-date installation of R and Bioconductor packages

**TO DO: copy text from Unibas R course!!!** 
**Add script to install all required packages** See `install_packages.R` from last year
**Add info on how to clone repository**
**host all scripts on Next Cloud: https://io.scicore.unibas.ch/?**
**Section: A refresher on DE Analysis with DESeq2/limma? as Davide did last year?**
