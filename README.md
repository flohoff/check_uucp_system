# check_uucp_system

Nagios plugin for checking a UUCP system. 

It should go to CRITICAL if it failed to login on last call.
It should go to CRITICAL if the last try/login is longer then x seconds ago



	check_uucp_system -s system -w warning -c critical

	 -?, --usage
	   Print usage information
	 -h, --help
	   Print detailed help screen
	 -V, --version
	   Print version information
	 --extra-opts=[section][@file]
	   Read options from an ini file. See https://www.monitoring-plugins.org/doc/extra-opts.html
	   for usage and examples.
	 -s, --system=uucp system name
	 -c, --critical=INTEGER
	 -w, --warning=INTEGER
	 -t, --timeout=INTEGER
	   Seconds before plugin times out (default: 15)
	 -v, --verbose
	   Show details for command-line debugging (can repeat up to 3 times)

# Example

	flo@p5:~$ ./check_uucp_system -s pax
	uucp_system CRITICAL - System pax 208 seconds ago failed: Login failed pax 


