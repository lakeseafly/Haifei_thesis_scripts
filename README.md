## Supplementary Notes for Haifei's thesis: Construction and analysis of the pangenomes of Amborella trichopoda and soybean and a comparative pangenomic study in flowering plants with different evolutionary histories

## Pangenome analysis pipeline

The pangenome analysis pipeline used in my thesis has been summarised and demonstrated as a published book chapter "Legume Pangenome Construction Using an Iterative Mapping and Assembly Approach", which can access by the DOI: https://doi.org/10.1007/978-1-0716-0235-5_3.

## Remove_reads_with_Ns.py

This script is used to remove paired raw reads with unknown bases (Ns) as these reads will affect the performance of mapping and end up in the pool of unmapped reads – the assumption being that the sequencing run’s quality was good enough to have only few reads with Ns.

Usage:`python Remove_reads_with_Ns.py [--cutoff CUTOFF] R1 R2`

## splitUp.py

This script is used to split the unmapped fastq files into R1, R2 and singlets for assembly by MaSuRCA. 

Usage: `python splitUp.py R1.fastq R2.fastq`

This will create three files, one with the R1, one with the R2, and one with the singlets. Use all three in Masurca
