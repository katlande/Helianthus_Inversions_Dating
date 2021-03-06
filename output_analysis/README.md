**Analyze the SNAPP output**

SNAPP outputs several files, but for our purposes the only important one is [example.log](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/output_analysis/example.log), which can
be converted into a [csv file](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/output_analysis/example.csv) containing the distribution of factors, including tree height, from all SNAPP runs.

To estimate divergence time, a [control csv file](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/output_analysis/Annuus_Argophylus_Control.csv) was previously generated by running SNAPP on non-inverted regions of two *Helianthus* species
with a [known divergence time](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1558-5646.2011.01537.x) of 1MYA. 

Using this control to calibrate tree height into a measurement of MYA, the age of the inversion of interest, as well as the confidence intervals in MYA, can be [calculated in R](https://github.com/katlande/Helianthus_Inversions_Dating/blob/master/output_analysis/Example%20Inversion%20Divergence.Rmd). 

For the example dataset, results should look like this:

![](https://raw.githubusercontent.com/katlande/Helianthus_Inversions_Dating/master/output_analysis/Example_Inversion_Age.png)
