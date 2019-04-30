# Helianthus_Inversions_Dating

**Each inversion was dated using SNP data from within the inverted regions of 20-60 *Helianthus* individuals in the BEAST2 package [SNAPP](https://github.com/BEAST2-Dev/SNAPP).**

For each comparison in SNAPP, individuals from populations polymorphic for the inversion of interest were chosen. Only homozygotes were used in this analysis. A SNAPP dating analysis follows the below pipeline, here using a small dataset called **example**:

1. Using a VCF containing the biallelic SNPs from the inverted region of the genome of the individuals to be analyzed, the VCF **LINK** is converted into a fasta file **LINK** of SNPs using the vcf2fasta perl script **LINK** and the following code:
`zcat example.vcf.gz | perl vcf2fasta.pl > example.fa`.

2. Next, the fasta is converted into an XML file **LINK** using the following code: 
`perl 500fasta2SNAPPxml.pl example.fa hapoltype.txt > example.xml`

The output file will be a ready-to-analyze XML file wherein each individual is sorted by haplotype.
- 500fasta2SNAPPxml.pl **LINK** converts fasta files into XML files for SNAPP analysis
- haplotype.txt **LINK** is a list of the haplotypes of each individual in the fasta

**NOTE: this code generates an XML file with priors specific to Helianthus dating. For other lineages, the perl file *500fasta2SNAPPxml.pl* would need to be modified, or XMLs can be generated from fastas using [BEAUti](https://github.com/CompEvol/beast2/tree/master/src/beast/app/beauti)**

3. XMLs can be analyzed in SNAPP, which outputs a log file. Log files can be checked in [Tracer](https://github.com/beast-dev/tracer) to ensure the SNAPP analysis had a high effective sample size and that the traces from the log file converge properly. 

4. Log files are then converted to csv files and analyzed in R using the following code **LINK**. Divergence time is calibrated using SNAPP runs from SNP data outside the inverted regions of species with known divergence times. **LINK to .csv of Ann/Arg run** 
