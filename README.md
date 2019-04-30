# Helianthus_Inversions_Dating

**Each inversion was dated using SNP data from within the inverted regions of 20-60 *Helianthus* individuals in the BEAST2 package [SNAPP](https://github.com/BEAST2-Dev/SNAPP).**

For each comparison in SNAPP, individuals from populations polymorphic for the inversion of interest were chosen. Only homozygotes were used in this analysis. A SNAPP dating analysis follows the below pipeline, here using a small dataset called **example**:

1. Using a VCF containing the biallelic SNPs from the inverted region of the genome of the individuals to be analyzed, the [VCF is converted into a fasta file](https://github.com/katlande/Helianthus_Inversions_Dating/tree/master/vcf_to_fasta).

2. [The fasta must next be converted into a SNAPP XML file in order to be analyzed](https://github.com/katlande/Helianthus_Inversions_Dating/tree/master/fasta_to_xml). 

3. XMLs can be analyzed in SNAPP, which outputs a log file. Log files can be checked in [Tracer](https://github.com/beast-dev/tracer) to ensure the SNAPP analysis had a high effective sample size and that the traces from the log file converge properly. 

4. Using this log file, a [divergence time can be estimated against SNAPP runs of *Helianthus* sequences with known divergence times](https://github.com/katlande/Helianthus_Inversions_Dating/tree/master/output_analysis). 
