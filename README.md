
Working as a postdoc, staff scientist or bioinformatician requires not only strong technical skills, but also the independence to pick up new workflows quickly.  Here in the Center for Disease Neurogenomics at the [Icahn School of Medince at Mount Sinai](https://icahn.mssm.edu), we work with a broad range of functional genomic datasets from human brain tissue.  One of the first analyses we run on a dataset is a variance partitioning analysis to identify study variables that are correlated with gene expression.  Many colleagues at Sinai and other institutions use this software pretty regularly in genomics applications.        

Since this analysis is a common task in our work, we have found that candidates who have the independent motivation to get this analysis up and running are likely to be successful in their new role in our group.  

I’ve given this test to many candidates over the last few years. It is deliberately open-ended, because that is what starting a functional genomics project is often like.  

# Assignment 
1) Read variancePartition [manuscript](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-016-1323-z) and install the software from the [Bioconductor page](http://bioconductor.org/packages/variancePartition/) 
 
2) Apply it to [ImmVar](10.1126/science.1249547) dataset and describe what you learned about biology of gene expression
    
3) How would you apply this framework to a biological question you are interested in?
 

Data from ImmVar (below) used in Figure 4 of the variancePartition manuscript.

### Original data is described here
Raj, et al, 2014. Polarization of the effects of autoimmune and neurodegenerative risk alleles in leukocytes. Science [doi:10.1126/science.1249547](https://pubmed.ncbi.nlm.nih.gov/24786080/)

De Jager, et al, 2015. ImmVar project: Insights and design considerations for future studies of "healthy" immune variation. Seminars in Immunology.   
    [doi:10.1016/j.smim.2015.03.003](https://pubmed.ncbi.nlm.nih.gov/25819567)
 
# Data for analysis in R
The data available from [https://hoffmg01.hpc.mssm.edu/ImmVar/](https://hoffmg01.hpc.mssm.edu/ImmVar/)

* user: rnaseq
* password: immvar
 
This is just formatted data I downloaded from [GEO:GSE56035](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE56035). Everything was open and public to begin with.

The data is stored in a binary format readable with

```r
info = readRDS('info.RDS')
ppData = readRDS('exprObj.RDS')
```

The dataset is fairly large, so if you machine has < 8Gb memory, you can do the analysis on a subset of a few thousand genes.
















