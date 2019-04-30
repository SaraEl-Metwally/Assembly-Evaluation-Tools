# Assembly-Evaluation-Tools
<p align="justify">
In order to repliacte the assembly evaluation results presented in our paper " A roadmap to sequence assembly evaluation tools ", we created this repository.

### Assembly evaluation tools
1. [Assemblathon](https://github.com/KorfLab/Assemblathon)
2. [GAGE](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz)
3. [QUAST](https://sourceforge.net/projects/quast/files/quast-5.0.2.tar.gz)
4. [CGAL](https://pachterlab.github.io/cgal/)
5. [REAPR](https://www.sanger.ac.uk/science/tools/reapr)

### Data Set:
The evaluation tools vary in their input files, we used the following input files with the benchmarked assembly evaluation tools:
1. Reference genome file for S. aureus data set genome size= 2903081bp, [genome.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/genome.fasta).
2. Contigs assembly files produced by Velvet assembler, [genome.ctg.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus).
3. Scaffolds assembly files produced by Velvet assembler, [genome.scf.fasta](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus).
4. Sequencing library 1 (fragments with average reads length 101bp, insert length 180bp, and no. of reads = 1,294,104),          [frag_1.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/frag_1.fastq.gz) and [frag_1.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/frag_2.fastq.gz).
5. Sequencing library 2 (short jumps with average reads length 37bp, insert length 3500bp, and no. of reads = 3,494,070),          [shortjump_1.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/shortjump_1.fastq.gz) and [shortjump_2.fastq](http://gage.cbcb.umd.edu/data/Staphylococcus_aureus/Data.original/shortjump_2.fastq.gz).

### Assemblathon evaluation tool
1. Download [assemblathon_stats.pl](https://github.com/KorfLab/Assemblathon/blob/master/assemblathon_stats.pl) script from assemblathon website and run the following command line:<br/> `perl assemblathon_stats.pl -genome_size 2903081 genome.scf.fasta` 

### GAGE evaluation tool 
1. Download [MUMmer 3.23](http://sourceforge.net/projects/mummer/files%2Fmummer%2F3.23/)
2. tar xvzf MUMmer3.23.tar.gz
3. make
4. Download [GAGE evaluation scripts](http://gage.cbcb.umd.edu/results/gage-validation.tar.gz) in the same folder. 
5. tar xvzf gage-validation.tar.gz
6. run the following command `sh getCorrectnessStats.sh genome.fasta genome.ctg.fasta genome.scf.fasta`
 
### QUAST evaluation tool 
1. Download [QUAST]((https://sourceforge.net/projects/quast/files/quast-5.0.2.tar.gz)
2. tar -xzf quast-5.0.2.tar.gz
3. cd quast-5.0.2
4. run the following command `./quast.py genome.scf.fasta -r genome.fasta`
5. display the summary of QUAST evaluation results using the following command: <br/> `less quast_results/latest/report.txt` 

### CGAL evaluation tool
1. Download [Bowtie2](https://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.3.5.1/) and you can use the binaries directly for Intel x86_64 architecture (https://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.3.5.1/bowtie2-2.3.5.1-linux-x86_64.zip/download).
