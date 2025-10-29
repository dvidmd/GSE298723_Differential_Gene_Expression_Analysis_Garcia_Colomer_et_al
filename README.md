# GSE298723_Differential_Gene_Expression_Analysis_Garcia_Colomer_et_al

Bioinformatic analysis of RNA-seq

RNA was sent to Novogene for RNA sequencing. Libraries were prepared using Illumina’s mRNA-Seq Poly(A) selection protocol and sequenced on a NovaSeq platform (paired-end 150 bp, unstranded) with a depth exceeding 20 million reads per sample. Initial quality filtering was performed by Novogene prior to delivery of clean reads. Raw reads were filtered according to the following criteria: removal of reads containing adapter sequences, removal of reads in which ambiguous nucleotides (N) constituted more than 10% of either read, and removal of reads in which more than 50% of bases had a Phred quality score ≤ 5.

The strandedness of the libraries was verified using how_are_we_stranded_here and read quality was assessed with FastQC (v0.12.1). Samples were aligned to the Genome Reference Consortium Mouse Build 39 (GRCm39) with Ensembl annotation release 104 using STAR (v2.7.9a). Gene quantification was computed using HTSeq (v.0.13.5) and normalization was performed using DESeq2 (v.1.34.0) in R (v.4.2.2). Differentially expressed genes were identified using an adjusted q-value < 0.05 and absolute fold change > 1.5 (Benjamini–Hochberg correction). All heatmaps, principal component analyses and volcano plots were produced in R (v4.1.2) using tidyverse (v2.0.0), dplyr (v1.1.4), tibble (v3.2.1), ComplexHeatmap (v2.10.0), ggplot2 (v4.0.0) and ggrepel (v0.9.3), then refined and exported using circlize (v0.4.16), viridisLite (v0.4.2) and svglite (v2.1.3).

Gene Ontology (GO) analyses were conducted using the DAVID functional-annotation platform (Database for Annotation, Visualization, and Integrated Discovery; https://david.ncifcrf.gov/tools.jsp), as described. 

All analyses were executed within a reproducible environment managed through Conda (v4.8.3) to ensure version control and computational reproducibility, and performed within RStudio (Build 467).

#############
## SAMPLES ##
#############

#ID	run	condition	strand
#E15_KO_NT	E15_KO_NT_htseq	KO_NT	Unstranded
#E15_KO_P	E15_KO_P_htseq	KO_P	Unstranded
#E15_KO_R24	E15_KO_R24_htseq	KO_R24	Unstranded
#E15_KO_R3	E15_KO_R3_htseq	KO_R3	Unstranded
#E15_WT_NT	E15_WT_NT_htseq	WT_NT	Unstranded
#E15_WT_P	E15_WT_P_htseq	WT_P	Unstranded
#E15_WT_R24	E15_WT_R24_htseq	WT_R24	Unstranded
#E15_WT_R3	E15_WT_R3_htseq	WT_R3	Unstranded
#E29_KO_NT	E29_KO_NT_htseq	KO_NT	Unstranded
#E29_KO_P	E29_KO_P_htseq	KO_P	Unstranded
#E29_KO_R24	E29_KO_R24_htseq	KO_R24	Unstranded
#E29_KO_R3	E29_KO_R3_htseq	KO_R3	Unstranded
#E29_WT_NT	E29_WT_NT_htseq	WT_NT	Unstranded
#E29_WT_P	E29_WT_P_htseq	WT_P	Unstranded
#E29_WT_R24	E29_WT_R24_htseq	WT_R24	Unstranded
#E29_WT_R3	E29_WT_R3_htseq	WT_R3	Unstranded
#E31_KO_NT	E31_KO_NT_htseq	KO_NT	Unstranded
#E31_KO_P	E31_KO_P_htseq	KO_P	Unstranded

References:

  Anders, S., Pyl, P. T., & Huber, W. (2015). HTSeq-a Python framework to work with high-throughput sequencing data. Bioinformatics, 31(2), 166–169. https://doi.org/10.1093/bioinformatics/btu638

  Bray, N. L., Pimentel, H., Melsted, P., & Pachter, L. (2016). Near-optimal probabilistic RNA-seq quantification. Nature Biotechnology, 34(5), 525–527. https://doi.org/10.1038/nbt.3519

  Dobin, A., Davis, C. A., Schlesinger, F., Drenkow, J., Zaleski, C., Jha, S., Batut, P., Chaisson, M., & Gingeras, T. R. (2013). STAR: ultrafast universal RNA-seq aligner. Bioinformatics, 29(1), 15–21. https://doi.org/10.1093/bioinformatics/bts635

  Conda Team. (2021). Conda: Package, dependency and environment management for any language (Version 4.8.3) [Computer software]. Anaconda, Inc. Zenodo. https://doi.org/10.5281/zenodo.4774216

  Everaert, C., Luypaert, M., Maag, J. L. V., Cheng, Q. X., Dinger, M. E., Hellemans, J., & Mestdagh, P. (2017). Benchmarking of RNA-sequencing analysis workflows using whole-transcriptome RT-qPCR expression data. Scientific Reports, 7, 1559.   https://doi.org/10.1038/s41598-017-01617-3

  Love, M. I., Huber, W., & Anders, S. (2014). Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. Genome Biology, 15(12), 550. https://doi.org/10.1186/s13059-014-0550-8

  Signal, B., & Kahlke, T. (2022). how_are_we_stranded_here: quick determination of RNA-Seq strandedness. BMC Bioinformatics, 23, 49. https://doi.org/10.1186/s12859-022-04572-7
#E31_KO_R24	E31_KO_R24_htseq	KO_R24	Unstranded
#E31_KO_R3	E31_KO_R3_htseq	KO_R3	Unstranded
#E31_WT_NT	E31_WT_NT_htseq	WT_NT	Unstranded
