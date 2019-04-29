# Helianthus_Inversions_Dating

**Each inversion was dated using SNP data from within the inverted regions of 20-60 *Helianthus* individuals in the BEAST2 package [SNAPP](https://github.com/BEAST2-Dev/SNAPP).**

For each comparison in SNAPP, individuals from populations polymorphic for the inversion of interest were chosen. Only homozygotes were used in this analysis. A SNAPP dating analysis follows the below pipeline:

1. Using a VCF containing the biallelic SNPs from the inverted region of the genome of the individuals to be analyzed, the SNP data is first converted into a .fasta file using **THIS CODE**.

2. Next, .fastas are converted into .XML files using the following code: `perl 500fasta2SNAPPxml.pl input.fa hapoltype.txt > output.xml`
The output file will be a ready-to-analyze XML file wherein each individual is sorted by haplotype.
- 500fasta2SNAPPxml.pl **LINK** converts fasta files into XML files for SNAPP analysis
- input.fa is the fasta of SNPs within the inversion of each individual to be analyzed
- haplotype.txt **LINK** is a list of the haplotypes of each individual in the fasta
- output.xml is the output xml file that can be analyzed by BEAST

An example output XML can be found here **LINK**.

3. XMLs can be analyzed in SNAPP. Each output .log file is checked in [Tracer](https://github.com/beast-dev/tracer) to ensure it has a high effective sample size and that the traces from the log file converge properly. 

4. .Log files are then converted to .csv files and analyzed in R using the following code **LINK**. Divergence time is calibrated using SNAPP runs from SNP data outside the inverted regions of species with known divergence times. **LINK to .csv of Ann/Arg run** 
