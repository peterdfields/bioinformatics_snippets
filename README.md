## Repo for tracking useful snippets which are often useful for lots of different bioinformatics tasks

#### remap reads in bam format to another reference using bwa mem (assumes position/coordinate sorted bam as input)
`samtools collate -uOn128 old.bam tmpxyz | samtools fastq - | bwa mem -pt16 ref.fa - | samtools sort --threads=4 -m4G -o new.bam`

#### subset bam by a list of contigs rather than using -L option (which is super slow). Create a list of target molecules called subset.lst and then
`samtools view -b whole_genome.bam $(<subset.lst) > subset.bam`
