# FrameshiftFinder

Work in progress!

* concept to input nucleotide sequence file containing at least two sequences in fasta format. 
* Translate nucleotide sesquences to protein sequence (using correct translation table). 
* Align both nucleotide and protein sequences. 
* Score alignments
* Iterate through the nucleotide alignment looking for gaps < 3 bp long (i.e. possible frameshift)
* At each gap site, delete one nucleotide, retranslate and realign the protein translation. 
* Score the new protein alignment and compare it to the orginal. If the revised alignment is better report this as a potentional frameshift.
* Alternatively if the alignment is worse delete two nucleotides at the orginal gap site and try gain. 
* If the revised alignment is better report this as a potentional frameshift.
* If not move on to the next gap. 
* Continue for all sequences in alignment. 
* Need to consider internals stops (maybe ignored in the alignment?) 
* Need to consider how this scales up to large inputs. May want to remove identical sequences or cluster the sequences to reduce the input file size. 

*example input file missingcytb.fsa
*example translated protein sequences missingcytb.pro
*example alignments in clustal format misssingcytb_nuc.aln and missingcytb_pro.aln
