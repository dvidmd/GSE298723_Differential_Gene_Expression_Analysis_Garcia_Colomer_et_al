# GSE298723_Differential_Gene_Expression_Analysis_Garcia_Colomer_et_al

RNA-seq differential expression was performed with DESeq2 (v1.34.0) in R (v4.2.2). The contrasts tested were: (1) WT_NT vs KO_NT, (2) KO_NT vs KO_P, (3) KO_NT vs KO_R3, and (4) KO_NT vs KO_R24. These correspond to the analyses reported in Figure 2 and Supplementary Figure S2 of García-Colomer et al.

Bioinformatic analysis of RNA-seq:

RNA was sent to Novogene for RNA-seq analysis. Libraries were prepared using Illumina’s mRNA-Seq PolyA selection protocol and sequenced on a NovaSeq platform (paired-end 150 bp, unstranded) with a depth exceeding 20 million reads per sample. Initial quality filtering was performed by Novogene prior to delivery of clean reads. Raw reads were filtered according to the following criteria: removal of reads containing adapter sequences, removal of reads in which ambiguous nucleotides (N) constituted more than 10% of either read, and removal of reads in which more than 50% of bases had a Phred quality score ≤ 5.

The strandedness of the libraries was verified using how_are_we_stranded_here and read quality was assessed with FastQC (v0.12.1). Samples were aligned to the Genome Reference Consortium Mouse Build 39 (GRCm39) with Ensembl annotation release 104 using STAR (v2.7.9a). Gene quantification was computed using htseq (v.0.13.5) and normalization was performed using DESeq2 (v.1.34.0) in R (v.4.2.2). Differentially expressed genes were identified using an adjusted q-value < 0.05 and absolute fold change > 1.5 (Benjamini–Hochberg correction). All heatmaps, principal component analyses and volcano plots were produced in R (v4.1.2) using tidyverse (v2.0.0), dplyr (v1.1.4), tibble (v3.2.1), ComplexHeatmap (v2.10.0), ggplot2 (v4.0.0) and ggrepel (v0.9.3), then refined and exported using circlize (v0.4.16), viridisLite (v0.4.2) and svglite (v2.1.3).

Gene Ontology (GO) analyses were conducted with the DAVID functional-annotation platform (Database for Annotation, Visualization, and Integrated Discovery; https://david.ncifcrf.gov/tools.jsp), as described. 
All analyses were executed within a reproducible environment managed through Conda (v4.8.3) to ensure version control and computational reproducibility, and performed within RStudio (Build 467).
