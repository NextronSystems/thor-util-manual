.. role:: raw-html-m2r(raw)
   :format: html

Diagnostics
===========

If THOR does not behave as expected, for example if it uses more
resources than expected, takes a long time to finish a scan, or exits
unexpectedly with a generic error, you can create a diagnostics pack for
Nextron Support.

Create the diagnostics pack with THOR Util's diagnostics command.

.. code:: doscon
 
   C:\thor>thor-util.exe help diagnostics

   Create diagnostics pack

   Usage:
     thor-util diagnostics [flags]

   Flags:
     -h, --help        help for diagnostics
     --output string   File to write diagnostics pack to (default "[...]\diagnostics.zip")
     --run             Rerun last THOR scan with debug logging before collecting diagnostics pack

By default, THOR Util writes the ``diagnostics.zip`` file to THOR's
working directory. The location is printed on the command line after data
collection finishes and can be changed with the ``--output`` flag.

Get diagnostics for a running THOR scan
---------------------------------------

The preferred way to collect THOR diagnostics is to run THOR Util's
diagnostics command while the issue is occurring. Use this method if you
suspect that THOR is stuck during a scan, that THOR has high memory or
CPU usage, or that another issue occurs during runtime.

.. code:: doscon

   C:\thor>thor-util.exe diagnostics

Get diagnostics for a finished THOR scan
----------------------------------------

If the THOR run has already finished or stopped unexpectedly, you can
also use the diagnostics command shown above. However, only a limited
amount of diagnostic data can be collected after the scan has ended. In
those cases, use the ``--run`` flag to rerun the last THOR scan. The
``--run`` flag is the preferred method if THOR exits unexpectedly or
intermittently.

.. code:: doscon

   C:\thor>thor-util.exe diagnostics --run

What data is collected
----------------------

THOR Util's diagnostics function collects the following data:

- A log of the THOR Util diagnostics run
- Go profiles for CPU, memory, and goroutines, see: https://go.dev/blog/pprof
- THOR's running configuration parameters
- A process list of all running processes on the machine. This helps
  identify processes that might interfere with THOR, such as an AV/EDR.
- A process dump of the running THOR instance
- The progress state of the running THOR instance
- A dump of the THOR DB
- The latest THOR log

.. hint::
   Critical or personal information may be present in the THOR log, THOR DB dump,
   running process list, in the THOR process dump, and in the progress report
   (working item details like path information). The profiles may indicate what
   type of data is being scanned but do not contain specific pieces of data.

The diagnostics pack is only used to investigate the issue you are facing
with THOR and will be deleted from our systems after the root cause has
been identified.
