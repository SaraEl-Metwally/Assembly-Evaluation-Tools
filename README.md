# Assembly-Evaluation-Tools
<p align="justify">
In order to repliacte the assembly evaluation results presented in our paper " A roadmap to sequence assembly evaluation tools ", we created this repository.</p> 

## Data set
We used a real benchmark dataset (S. aureus, genome size= 2903081bp) from [GAGE website](http://gage.cbcb.umd.edu/data/index.html). There are two sequencing libraries for this data set, one is fragmented with average read length 101bp and the other is short jump with average read length 37bp. The [reference genome](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/genome.fasta) for S. aureus data set is provided to some reference based evaluation tools to compute various accuarcy metrics. We extracted the [Contigs/Scaffolds](http://gage.cbcb.umd.edu/results/index.html) produced by Velvet assembler and ran the following assembly evaluation tools:[Assemblathon](https://github.com/KorfLab/Assemblathon), [GAGE](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz), [QUAST](https://sourceforge.net/projects/quast/files/quast-5.0.2.tar.gz), and [CGAL](https://pachterlab.github.io/cgal/). 

### Assemblathon evaluation tool
1. Download [assemblathon_stats.pl](https://github.com/KorfLab/Assemblathon/blob/master/assemblathon_stats.pl) script from assemblathon website and run the following command line:<br/> `perl assemblathon_stats.pl -genome_size 2903081 genome.scf.fasta` 

### GAGE evaluation tool 
1. Download [MUMmer 3.23](http://sourceforge.net/projects/mummer/files%2Fmummer%2F3.23/)
2. tar xvzf MUMmer3.23.tar.gz
3. make
4. Download [GAGE evaluation scripts](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz) in the same folder. 
5. tar xvzf gage-validation.tar.gz
6. run the following command `sh getCorrectnessStats.sh genome.fasta genome.ctg.fasta genome.scf.fasta`
 
