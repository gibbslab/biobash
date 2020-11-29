## BIOBASH Vb0.1
Bogotá - Colombia Octubre 4 2020

## INFO FOR DEVELOPERS
This is the b0.1 version of BIOBASH (BB), a set of scripts for common tasks in bioinformatics.
The development behind BB is based on a couple of key ideas:

1) A script must rely ONLY on BASH and their "core" utils, for example the use of
AWK or sed is allowed but not the use of PERL or any other "external" scripting language. Nevertheless the idea of having
a BB wrapper for other tools is acceptable, in that case the script shall check its own requirements and inform user accordingly.

2) To be part of BB, an script should be useful in the common, daily bioinformatics practice,
so things like "lists management", "file conversions/processing" useful in the field
are also welcome. Nevertheless if you feel like re-writing the BLAST algorithm in bash... go ahead!

3) BB is based on specific tasks. A given task must do ONLY ONE task, of course
most of the times it will be necessary to write long or somehow complex pipes so the
script can be operative, but at the end as a whole it performs just one task.
To clarify the point, a script that takes a multiple fasta file, split it in single files, 
and then gets the GC content for each of the splitted files, should be written as two separate functions.
One that splits the file and another one that gets the GC content for each splitted file.
Nevertheless, if you want to write a script that  outputs the GC content (in a table for example) for a set of
fasta entries in a multiple fasta file it is ok to write that function alone.

In upcoming releases there exists the possibility to create Workflows based on BB functions (perhaps using nextflow also)
that will carry this type of functionalities also but they should be written in a separate section.

4) Although we haven't defined a coding style itself one "rule" is that each function name
MUST begin with  "bb_" and then the name of the function, with no spaces but underscores.
One important aspect is that the name of the function have to clearly describe its
functionality, no matter how long the name will be, so names like:

``$ bb_display_histogram_of_frequencies``
		

are in any case better than:

``$bb_histogram or bb_get_histogram``

Try to use keywords that reflect what the function does, the use of "get", "extract", "convert", "transform" and "display"
in the names of the functions are higly encouraged.


5) By default, running a BB tool without arguments will display the help. Please refer to
the already written functions for examples.

6) There are special "common" scripts  which will hold common routines to
be used for any script, for instance: bb_create_tmp_file, should be used for any script that will need a temporary file for its operation.

7)Comments. Please use as much commentaries in the code as you find necessary, if 
in doubt it is _always_ better to comment the code that not to.

8) Release: the official release will be created and liberated by the main developer.

9) Last but not least, routines should work on any UNIX based machine (yes, including OSX).
If not, if impossible, please ask for help o please make it clear for the final user somehow.

NOTE: 
Some useful resources to stablish a set of coding rules can be found here:
https://github.com/progrium/bashstyle
http://wiki.bash-hackers.org/scripting/obsolete
 
Code that can be migrated:
https://github.com/sdwfrost/biobash


## DIRECTORY STRUCTURE

* INSTALL: installation instructions, for final users.
* README.developer: this file.
* README: Readme file for final users.
* source: Contains source code.
* test: data files for testing BB.


## DEVELOPERS

Andres Pinzon (ampinzonv@unal.edu.co)
Nicolás Gomez (x)ngomezca@unal.edu.co)
Nicolás Mendoza (nimendozam@unal.edu.co)

