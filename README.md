# ATAC-Seq-pipeline
A pipeline of ATAC-Seq raw data processing and downstream analysis
### Options:
    -h --help      display the usage and exit.
    -a --access    necessary file containing SRR number or sample name to be operate. [e.g. accession.txt]
    -d --dump      transform sra to fastq by fastq-dump.
    -f --fastp     perform QC to sample by fastp with the default parameters,the sequencing type P/S must be provided.(Pair end and Single end) [e.g. P/S]
    -c --cut       specify two comma separated INT parameters to cutadapte for sample. [e.g. 15,0]
    -b --bowtie2   use bowtie2 to map the clean data to the REFERENCE and transform to the bam file
    -s --sort      use samtools to sort the bam file
    -p --picard    use picard to remove duplicates
    -r --remove    remove unwanted reads using samtools
    -D --deeptools use deeptools to get BigWiggle from sorted bam for drawing gene profile
    -P --peaks     use macs2 to call peaks from filtered bam
    -H --HOMER     use HOMER to find Motifs and TFBS
    -g --graph     transform to bigWig Format for genome browser
    -v --version   display version information and exit.\n"

### Example
sh ATAC_pipeline.sh -a accession.txt -d -f S -c 5,3 -b -s -p -r -D -P -H -g
