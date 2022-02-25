---
permalink: /software/
title: "Software"
---

I'm primarily interested in extracting biological insights from the vast 'Omics datasets being generated, but to do this we require efficient and user-friendly tools. I have developed two packages: <i>packFinder</i>, an R pipeline for the annotation a particular type of DNA transposon based on sequence features, and <i>MetaboBlend</i>, a Python workflow for the elucidation of small molecules in mass-spectrometry metabolomics.

# packFinder <img src="https://raw.githubusercontent.com/jackgisby/packFinder/master/inst/packFinder_hex.png" alt="packFinder-hex-logo" align="right" hspace=15px style="width:172.67px;height:200px;"> 

Previous papers investigating Pack-TYPE transposons, transposable elements (TEs) that capture chromosomal loci and genes, have been based on ad-hoc pipelines for their annotation. They have mostly been focussed on Mutator-like elements that have relatively long terminal inverted repeats and target site duplications, making recognition of these elements relatively simple. <i>packFinder</i> permits the systematic investigation of Pack-TYPE TEs for any TIR-based family in any genome and improves the replicability of the annotations. 

<i>packFinder</i> can be installed from Bioconductor as follows:

```r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("packFinder")
```

A tutorial for the common use of the package is available on the <a href="https://doi.org/doi:10.18129/B9.bioc.packFinder">Bioconductor website</a> and the code is available <a href="https://github.com/jackgisby/packFinder">on github</a>. 

We have employed the package for the annotation of Pack-TYPE TEs in multiple plant genomes for previously unreported families. A paper describing this work has now been published <a href="https://doi.org/10.1371/journal.pgen.1010078">in PLOS Genetics</a>. 

# MetaboBlend

Annotation of metabolites is a major bottleneck in untargeted metabolomics experiments. There are various methods available for automated structural elucidation, and there is a competition for this task, but the majority of these methods rely on metabolites being present in compound databases; despite the growing size of compound databases such as the human metabolite database, this may not be a realistic assumption. We are therefore developing <a href="https://github.com/computational-metabolomics/metaboblend"><i>MetaboBlend</i></a> to elucidate small molecules using chemical knowledge, without restricting the search to known compounds. We plan to release version 1.0 on PyPi shortly. 
