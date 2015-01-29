# fit
A command line tool to select files/directories to fill destination media completely.

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
