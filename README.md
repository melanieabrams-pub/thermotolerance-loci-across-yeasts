# thermotolerance-loci-across-yeasts
code for doi 10.1101/2020.08.31.275453 for RH-seq reanalysis and resampling of genotype sharing across thermotolerance loci in Saccharomyces yeast

README
The scripts in this repository are for doi 10.1101/2020.08.31.275453 for RH-seq reanalysis and resampling of genotype sharing across thermotolerance loci in Saccharomyces yeast

Reanalysis of RH-seq from Weiss et al., 2018
	* First, run published RH-Seq pipeline steps 1-4 from Weiss et al., 2018.
		Requirements: python2 environment, with pandas, numpy, re, and sys libraries.
	These scripts can be found at: https://github.com/weiss19/rh-seq
	* Then, run scripts 5-9 from this repository.  
		Additional requirements: python3 environment for script 9

Resampling of G1 and G12 from SelectionHapStats
	* First, run the published SelectionHapStats pipeline from Garud et al., 2015, Garud and Petrov 2016, Garud and Rosenberg 2015, and Harris et al., 2018.
		These scripts can be found at: https://github.com/ngarud/SelectionHapStats .  
		The vcf2SelectionHapStats script generates input formatted for the Garud pipeline from a gVCF file, as for the 1011 Yeast Genomes
		The vcf2SelectionHapStats_Bergstrom script generates input formatted for the Garud pipeline from a VCF file, as for the Bergstrom et al. 2014 data
	* Then, rank the h12_h2h1.py script output using the rank_g1 or rank_g12 script for g1 and g12 respectively.
	* Then, resample the output of H12_H2H1.py using either the resample_g1-or-g12.py.
		Additional requirements: python3 with statistics and random
