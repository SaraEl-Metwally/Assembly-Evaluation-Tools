# Assembly-Evaluation-Tools
<p align="justify">
In order to repliacte the assembly evaluation results presented in our paper " A roadmap to sequence assembly evaluation tools ", we created this repository.</p> 

## Data set
We used a real benchmark dataset (S. aureus, genome size= 2903081bp) from [GAGE website](http://gage.cbcb.umd.edu/data/index.html). There are two sequencing libraries for this data set, one is fragmented with average read length 101bp and the other is short jump with average read length 37bp. The [reference genome](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/genome.fasta) for S. aureus data set is provided to some reference based evaluation tools to compute various accuarcy metrics. We extracted the [Contigs/Scaffolds](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus) produced by Velvet assembler and ran the following assembly evaluation tools: [Assemblathon](https://github.com/KorfLab/Assemblathon), [GAGE](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz), [QUAST](https://sourceforge.net/projects/quast/files/quast-5.0.2.tar.gz), and [CGAL](https://pachterlab.github.io/cgal/). 

### Notes:
The evaluation tools vary in their input files, we used the following input file formats with the benchmarked assembly evaluation tools:
1. Reference genome file for S. aureus data set,[genome.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/genome.fasta).
2. Contigs assembly files produced by Velvet assembler, [genome.ctg.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus).
3. Scaffolds assembly files produced by Velvet assembler, [genome.scf.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus).
4. Sequencing library 1 (fragment with average reads length: 101bp, insert length: 180bp, and # of reads:1,294,104),          [frag_1.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/frag_1.fastq.gz) and [frag_1.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/frag_2.fastq.gz).

### Assemblathon evaluation tool
1. Download [assemblathon_stats.pl](https://github.com/KorfLab/Assemblathon/blob/master/assemblathon_stats.pl) script from assemblathon website and run the following command line:<br/> `perl assemblathon_stats.pl -genome_size 2903081 genome.scf.fasta` 

### GAGE evaluation tool 
1. Download [MUMmer 3.23](http://sourceforge.net/projects/mummer/files%2Fmummer%2F3.23/)
2. tar xvzf MUMmer3.23.tar.gz
3. make
4. Download [GAGE evaluation scripts](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz) in the same folder. 
5. tar xvzf gage-validation.tar.gz
6. run the following command `sh getCorrectnessStats.sh genome.fasta genome.ctg.fasta genome.scf.fasta`
 
