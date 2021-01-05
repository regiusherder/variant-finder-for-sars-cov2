# Variation Finder for SARS-CoV-2/COVID19
## Introduction
This python program is develpoed to identify any nucleotide mutations and accompanying amino-acid changes in diffrent protiens of SARS-CoV-2 (COVID19). Using aligned fasta sequences in text file format this python program can detect the variations in the SARS-CoV-2 (COVID19) isolate compared to the Wuhan_Hu_1 Reference Strain. The output file will contain the list of Nucleotide Changes with position in the SARS-CoV-2 genome. If the Nucleotide change leads to a amino acid change, it will also be listed with Amino acid in the reference sequence and Amino acid in the query sequence. The name of the protien in which the amino acid change occurs will also be listed with the position of amino acid in the protien. Though this program is written to identify the variants in the SARS-CoV-2  genome, it can be modified to find mutations in any other genomes with suitable reference sequence.

## How to use 

### 1. Make sure you have proper input file
This program takes in Query sequences in fasta format in a text file. (This repository also include sample Query sequences).
### 2. Launch the tool
You can try the variantfinder tool using :

    python3 variantfinder.py
   or
   

    python variantfinder.py

### 3. Enter the path of input and output files

 

    Enter query sequence filename : Input.fas #note you can also input a text file as long as the conents are in fasta format
    Enter output filename (along with .csv) : Output.csv

## Limitations

1) With regard to degenrate bases the amino acid change will be shown as "x".
2) Deletion type of mutations represented by "-" will not be considered.
3) Any insertion type mutation in any part of the Genome will lead to frame shift while calcuating the Amino acids.
