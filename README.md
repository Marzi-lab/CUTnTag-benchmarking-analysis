# CUT&Tag benchmarking and analysis

This repository holds code used to carry out processing, benchmarking and analysis of CUT&Tag against ENCODE ChIP-seq, as shown in our preprint ("CUT&Tag recovers up to half of ENCODE ChIP-seq histone acetylation peaks"; doi: https://doi.org/10.1101/2022.03.30.486382).  

The analysis consists of two main parts:
1) Pre-processing (adapter trimming, alignment, peak calling, etc.) and a few additional analyses (e.g. heatmap generation) using Linux command line scripts
2) Downstream processing in R

This demo was carried out on two real samples, Diagenode C15410196 (1:50) and CST9733, starting from fastq files. These files are too large to be hosted here but can be downloaded from the European Nucleotide Archive (sample accessions SAMN27024067 and SAMN27024069, respectively). All code required for processing and analysis is enclosed, and presented in a defined order where appropriate. Other outputs and smaller intermediate files have also been included where possible. The scripts assume a particular directory structure but note that base paths will need to be amended. A complete analysis may take up to 20 hours, depending on available resources and file sizes.  


The following command line tools were used:

- Cutadapt (version 1.18)
- TrimGalore (version 0.6.6)
- Bowtie (version 2.2.9)
- Picard (version 2.6.0)
- bedtools (version 2.25.0)
- deeptools (version 3.5.4)
- samtools (version 1.3.1)
- SEACR (version 1.3)
- MACS2 (version 2.2.9.1)
- HOMER (version 4.11.1)


The following R packages were used:

- GenomicRanges (version 1.50.2)
- IRanges (version 2.32.0)
- genomation (version 1.30.0)
- clusterProfiler (version 4.6.2)
- rtracklayer (version 1.58.0)
- chromVAR (version 1.20.0)
- ChIPseeker (version 1.34.1)
- DiffBind (version 3.8.4)
- BRGenomics (version 1.10.0)
- marge (version 0.0.4.9999)

Required R packages can also be found in the session information provided in the html file with downstream analysis. Note that this pipeline is now available in the form of the EpiCompare R package (https://github.com/neurogenomics/EpiCompare).


### References

CUT&Tag recovers up to half of ENCODE ChIP-seq histone acetylation peaks  
Leyla Abbasova, Paulina Urbanaviciute, Joy N Ismail, Di Hu, Brian M Schilder, Alexi Nott, Nathan G Skene, Sarah J Marzi  
bioRxiv 2022.03.30.486382; doi: https://doi.org/10.1101/2022.03.30.486382  
  
EpiCompare: R package for the comparison and quality control of epigenomic peak files (2022)  
Sera Choi, Brian M. Schilder, Leyla Abbasova, Alan E. Murphy, Nathan G. Skene  
bioRxiv 2022.07.22.501149; doi: https://doi.org/10.1101/2022.07.22.501149  

