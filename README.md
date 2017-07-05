     written by peteskene@gmail.com
     
     (1) takes in a bed file (can have any number of columns).
             - optionally finds midpoint and extends features (requires chr_sizes file found from species string)
             - optionally just extends each feature (requires chr_sizes file found from species string)
             
     (2) extract sequence data as a fasta file (requires path to whole_genome_fasta_file; entered as a string)
	     fasta file has no text wrapping (i.e. entire sequence for an id is on one line)
     
     (3) for each each feature in the fasta file it:
             - counts number of observed CpG dinucleotides
             - calculates the expected number of CpG (#C * #G)/length of sequence
             - calculates CpG observed/expected
             
     (4) inserts the CpG o/e into the original supplied bedfile and returns this as a pandas dataframe. 
     
     Note that the calculated CpG o/e is for the genomic region specified by the supplied parameters (e.g. extending flanks),
     but the original bed file co-ordinates are returned
 
