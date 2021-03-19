## Repo for tracking useful snippets which are often useful for lots of different bioinformatics tasks

#### remap reads in bam format to another reference using bwa mem (assumes position/coordinate sorted bam as input)
`samtools collate -uOn128 old.bam tmpxyz | samtools fastq - | bwa mem -pt16 ref.fa - | samtools sort --threads=4 -m4G -o new.bam`
