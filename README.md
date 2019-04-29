# Assembly-Evaluation-Tools
<p align="justify">
In order to repliacte the assembly evaluation results presented in our paper " A roadmap to sequence assembly evaluation tools ", we created this repository.</p> 

## Data set
We used a real benchmark dataset (S. aureus, genome size= 2903081bp) from [GAGE website](http://gage.cbcb.umd.edu/data/index.html). There are two sequencing libraries for this data set, one is fragmented with average read length 101bp and the other is short jump with average read length 37bp. We extracted the [Contigs/Scaffolds](http://gage.cbcb.umd.edu/results/index.html) produced by Velvet assembler and ran the following assembly evaluation tools:[Assemblathon](https://github.com/KorfLab/Assemblathon), [GAGE](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz), [QUAST](https://sourceforge.net/projects/quast/files/quast-5.0.2.tar.gz), and [CGAL](https://pachterlab.github.io/cgal/). 

### Assemblathon evaluation tool
1. Download assemblathon_stats.pl script from assemblathon website and ran the following command line: 
`perl assemblathon_stats.pl -genome_size 2903081 scaffolds.fasta` 

### GAGE evaluation tool 
1. Download [MUMmer 3.23](http://sourceforge.net/projects/mummer/files%2Fmummer%2F3.23/)
2. 
