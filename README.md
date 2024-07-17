# Unraveling Immunogenomic Diversity in Single-Cell Data

## Background and motivation

The human immune system is governed by a complex interplay of molecules encoded by highly diverse genetic loci. Immune genes such as B and T cell receptors, human leukocyte antigens (HLAs), and killer Ig-like receptors (KIRs) exhibit remarkable allelic diversity across populations. However, conventional single-cell analysis methods often overlook this diversity, leading to erroneous quantification of immune mediators and compromised inter-donor comparability.

## Description

To address these challenges and unlock deeper insights from single-cell studies, we present a comprehensive workflow comprising two software and one data packages (Figure 1):

1. **[scIGD](https://github.com/AGImkeller/scIGD)** (**s**ingle-**c**ell **I**mmuno**G**enomic **D**iversity): A Snakemake workflow designed to automate allele-typing processes for immune genes, with a focus on key targets like HLAs. In addition, it facilitates allele-specific quantification from scRNA-seq data using donor-specific references.

2. **[SingleCellAlleleExperiment](https://bioconductor.org/packages/SingleCellAlleleExperiment)**: This R/Bioconductor package maximizes the analytical potential of results obtained from *scIGD*. It offers a versatile multi-layer data structure, allowing representation of immune genes at various levels, from alleles to genes to functionally similar gene groups. This enables comprehensive analysis across different layers of immunologically-relevant annotation.

3. **[scaeData](https://bioconductor.org/packages/scaeData)**: An R/ExperimentHub data package housing three 10x datasets processed by *scIGD*. These datasets can be utilized to perform exploratory and downstream analysis using the novel *SingleCellAlleleExperiment* data structure.

![alt text here](https://github.com/ahmadalajami/scIGDWorkflowDemoBioC2024/blob/devel/inst/images/scIGD_SCAE_wokflow.png)

**Figure 1:** Overview of the *scIGD* workflow for unraveling immunogenomic diversity in single-cell data, highlighting the integration of the *SingleCellAlleleExperiment* package for comprehensive data analysis.

## Insights

Preliminary findings demonstrate accurate quantification of different HLA allele groups in (amplicon-based and whole-transcriptome-based) scRNA-seq datasets from diverse sources, including cancer patients and human atlas samples. This not only enhances the comparability of immune profiles across donors but also sheds light on population-specific susceptibilities to infections. Our work lays the groundwork for precise immunological analysis of multi-omics data, particularly in elucidating allele-specific interactions.

## BioC2024 demo

I intend to showcase all three tools, emphasizing the utilization of *SingleCellAlleleExperiment* and its functionalities on one of the example datasets available in *scaeData*, for exploratory and downstream analysis across the three layers offered by the data structure.

## Pre-requisites

- Basic knowledge of R syntax
- Familiarity with single-cell transcriptomic analyses, such as *[OSCA](https://bioconductor.org/books/OSCA)*
- Familiarity with *[SingleCellExperiment](https://bioconductor.org/packages/SingleCellExperiment)* and/or *[SummarizedExperiment](https://bioconductor.org/packages/SummarizedExperiment)*

## Participation

The format is a 45 minute session consisting of hands-on demos, exercises and Q&A.

Questions are welcome at any time. Contact details are listed at the bottom of the page.

## *R* / *Bioconductor* packages used

- `SingleCellAlleleExperiment`: https://bioconductor.org/packages/SingleCellAlleleExperiment
- `scaeData`: https://bioconductor.org/packages/scaeData

## Time outline

| Activity                                      | Time |
|-----------------------------------------------|------|
| Introduction                                  | 10m  |
| Overview of scIGD                             | 5m   |
| Overview of scaeData                          | 5m   |
| SingleCellAlleleExperiment + data analysis    | 25m  |

## Demo goals and objectives

### Learning goals

- Learn the constraints inherent in traditional single-cell analysis techniques and the importance of HLA allele-specific quantification
- Understand the difference between `SingleCellExperiment` and `SingleCellAlleleExperiment`
- Demonstrate how these tools can be applied and adopted to enhance existing workflows

### Learning objectives

- Perform allele typing to identify HLA alleles from genetic sequences in scRNA-seq data
- Achieve allele-specific quantification using donor-specific references
- Navigate through distinct layers within the data object for diverse representations of HLA genes
- Conduct exploratory data and downstream analyses across any of the layers offered by the data object

## Instructor name and contact information

- Ahmad Al Ajami \<alajami at med.uni-frankfurt.de>