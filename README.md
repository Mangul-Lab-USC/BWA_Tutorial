
# Sequence Alignment with BWA


1. Install BWA package, SAMTOOLS, reference and sequences to align:
git clone https://github.com/Mangul-Lab-USC/BWA_Tutorial.git
cd BWA_Tutorial/samtools
./configure
Make
Make install
cd ..

2. Create Reference Index:
bwa/bwa index reference.fa

3. Align Reads to Reference Genome:
bwa/bwa mem reference.fa sequences.fa > alignments.sam

4. Convert Sam file to Bam file:
samtools/samtools view -S -b alignments.sam > alignments.bam

5. View alignments that matched to reference sequence:
samtools/samtools view alignments.bam
samtools/samtools view –F 4 aligments.bam

