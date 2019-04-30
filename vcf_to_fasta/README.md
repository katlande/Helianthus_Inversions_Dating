##Convert your VCF into a fasta

Using a VCF of biallelic SNPs from the inverted region of the genome, a fasta file can be made using the [vcf2fasta perl script](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/vcf_to_fasta/vcf2fasta.pl) made by [Greg Owens](https://github.com/owensgl/wild_gwas_2018/blob/master/perl_tools/vcf2fasta_basic.pl). 


In this example, the raw [example VCF](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/vcf_to_fasta/example.vcf) can be converted to the [example fasta](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/vcf_to_fasta/example.fa) with the code `zcat example.vcf.gz | perl vcf2fasta.pl > example.fa`.
