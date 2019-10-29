
# Sequence Alignment with BWA


1. Install BWA package, SAMTOOLS, reference and sequences to align:
git clone https://github.com/Mangul-Lab-USC/BWA_Tutorial.git

2. Create Reference Index:
bwa/bwa index -p HIV_ref HIV_ref.fasta

3. Align Reads to Reference Genome:
bwa/bwa mem HIV_ref reads.fasta > reads.sam

4. View Alignments 
less reads.sam

