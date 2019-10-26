
# Sequence Alignment with BWA


1. Install BWA package, SAMTOOLS, reference and sequences to align:
git clone https://github.com/Mangul-Lab-USC/BWA_Tutorial.git
cd BWA_Tutorial/samtools
./configure
Make
Make install
cd ..

2. Create Reference Index:
bwa/bwa index -p HIV_ref HIV_RNA_Reference_Genome.fa

3. Align Reads to Reference Genome:
bwa/bwa mem HIV_ref human_sample_RNA.fa > alignments.sam


4. Convert Sam file to Bam file:
samtools/samtools view -S -b alignments.sam > alignments.bam

5. View alignments that matched to reference sequence:
samtools/samtools view alignments.bam

