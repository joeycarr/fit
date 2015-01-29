# fit

A command line tool to select files/directories to fill destination
media completely.

	usage: fit [-h] [-i n] [-q] dest src [src ...]
	
	Prints a list of source directories or files that will fill the destination
	directory with a minimum of leftover disk space.
	
	positional arguments:
	  dest                  The directory you're trying to fill.
	  src                   The directories or files you want to fit into the
	                        destination directory.
	
	optional arguments:
	  -h, --help            show this help message and exit
	  -i n, --iterations n  The number of times to attempt to improve the fit.
	                        Default is 2048.
	  -q, --quiet           Suppress message about the utilization of the target
	                        directory to the standard error.

The fit tool is a bespoke Python script used for filling 2.5 terabyte
LTO tapes to capacity with large media files. The program addresses
the tedium of manually selecting a combination of media files to limit
the leftover space on the LTO tape. Since a combinatorial approach to
find a best possible solution has too many posibilities to be
practically computable, the script optimizes the selection of files by
iteratively improving a random selection.

The script targets Python 2.7 on Mac computers, although it should
probably work on Linux as well, perhaps with a little modification.