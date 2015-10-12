eFISHent 2.0 Manual:

Introduction:

The software consists of two seprate PERL scripts:

1) perl_loop_mafft_all
This script aligns the .fas output files from bingene using MAFFT (must be installed globally on your Linux machine; http://mafft.cbrc.jp/alignment/software/linux.html)

2) countseqs2
This script will use the alignment files deposited in outfolder1 (ending in .fas.out) resulting from step 1) and will count the length of each sequence as well as the gaps to collect information on how fragments are distributed, what the total-, gap-, and true sequence lengths are and compute a score, to evaluate how well the sequences score, based on the missing data, compared to the query sequence for each alignment file.

How to run:

1) perl_loop_mafft_all

- Input: Input files are the resulting files from bingene (see Li et al. 2013), i.e. multiple fasta files containing sequence information from a query sequence and further sequences of interest and a list containing the fasta file names as text document, which should be named fileID.

Bingene input:
1st file:
>queryNew_8fish_Danio_rerio 
GTATCATCTCCTGAG
>Aal 
TACCAGCTCCTGAA
>D1-5 
TATCATCTCCTGAGG

2nd file:

>queryNew_8fish_Danio_rerio 
GTATCATCTCCTGAG
>Aal 
TACCAGCTCCTGAA
>D1-5 
TATCATCTCCTGAGG

(…)

fileID:
Danio_rerio.1.48788.48665.fas
Danio_rerio.1.296705.296829.fas


example command: 
perl perl_loop_mafft_all_com_scalar fileID outfolder1 outfolder2 


2) countseqs2.pl

- Input: 

