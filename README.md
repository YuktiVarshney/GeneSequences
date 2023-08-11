# GeneSequences
#A python project to calculate Non-DNA bases in a gene sequences 

#METHOD 1

def count_dna(seq, allowed_bases=['A','T','G','C']):
    seq = seq.upper()
    total_dna_bases = 0
    for base in allowed_bases:
        total_dna_bases = total_dna_bases + seq.count(base.upper())
    dna_fraction = total_dna_bases / len(seq)
    return(dna_fraction * 100)
print(count_dna("ACTRGATCYGATCGANTCGATG"))
print(count_dna("ACTRGATCYGATCGANTCGATG", ['A','T','C','G','N']))
print(count_dna("actgratcygtganctttgacg"))


#METHOD 2
from __future__ import division
seq = "ACTNGTGCTYGATRGTAGC"
allowed_bases = ["A", "T", "G", "C", "Y", "R"]
total_dna_bases = 0
for base in allowed_bases:
    total_dna_bases = total_dna_bases + seq.count(base)
dna_fraction = total_dna_bases / len(seq)
print(dna_fraction * 100)
