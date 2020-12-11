## BIOBASH Vb0.1

BIOBASH is a set of BASH scripts useful for common bioinformatics related tasks.
It was born by our group's necessity on performing simple rutinary tasks while working
on bioinformatics data analysis.
Therefore, these scripts cover different tasks that are not all necessarily "bioinformatics" tasks,
but "bioinformatics-related" tasks, such as data manipulation, data filtering and organization etc.

This project started as a weekend exercise in 2015 and then was kind of abandoned for several years (although the scripts developed have shown to be useful during these years!!!).

As for this release there are these routines:


### FASTA/FASTQ ANALYSIS AND MANIPULATION
* bb_count_seqs (Counts the number of sequences in a multiple fastq or fasta file)
* bb_extract_fasta_entry (Extracts a single sequence from a multiple fasta file)
* bb_get_fasta_headers (Extracts all fasta headers in a fasta file)
* bb_remove_fasta_header (Concatenates all files in a multiple fasta file)
* bb_count_residues (Counts the number of residues in a fasta file)
* bb_get_GC_content (Determines the %GC in a fasta file)
* bb_fastq2fasta (Converts a fastq file in a fasta file)
* bb_rename_fasta_entries (Sequentially renames all fasta entries in a multiple fasta file)
* bb_get_seq_length (Displays sequences length from a single/multiple fasta file)
* bb_split_fastq (Split forward and reverse reads of a fastq file)

### LISTS AND GENERAL FILE MANIPULATION
* bb_dos2unix (Removes non UNIX characters from a file)
* bb_get_freq_from_list (Obtains the frequency of every item in a list of items)
* bb_get_nr_list (Obtains a non redundant list from a redundant list of items)
* bb_remove_empty_lines (Removes empty lines from any file)
* bb_setup_project (Creates a directory structure for bioinformatics analysis)

By default calling any script without arguments will show a help menu.

### INSTALLATION (and UNISTALLATION)
Just run the "installbiobash" script in the top folder of this release (assuming you are at the root of the biobash folder):

``./installbiobash``

BY default this script attempts to install all scripts in /usr/local/bin, but you can
change this install directory during the installation process.
In order to avoid any conflict between BB scripts and other tools installed
in your systems, all scripts in BB begin with the "bb_" prefix, so if you
want to know whcih BB scripts are installed in your system just type "bb_" in your shell
and hit  the "TAB" key.
To uninstall BB, just run the command: 

``bb_uninstall_biobash``

And follow the instructions.


