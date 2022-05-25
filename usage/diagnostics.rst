.. role:: raw-html-m2r(raw)
   :format: html

Diagnostics
===========

If THOR does not behave like it should, e.g. using more resources than
you expected, taking more time with the scan as usual or unexpectedly
exits with a generic error, you can create a diagnostics pack for our
support to help in troubleshooting the issue.

This can be done using THOR Util's diagnostics command.

.. code:: none
 
   thor-util.exe help diagnostics

   Create diagnostics pack

   Usage:
     thor-util diagnostics [flags]

   Flags:
     -h, --help        help for diagnostics
     --output string   File to write diagnostics pack to (default "[...]\diagnostics.zip")
     --run             Rerun last THOR scan with debug logging before collecting diagnostics pack

By default the ``diagnostics.zip`` file is put in THOR's working
directory. The location is printed on the commandline in the end
of the data collection and can be changed using the ``--output`` flag.

Get diagnostics of a running THOR scan
--------------------------------------

The preferred method of collecting THOR diagnostics is to run THOR Util's
diagnostics command directly when the issue is occurring.

.. code:: none

   thor-util.exe diagnostics

Get diagnostics of a finished THOR scan
---------------------------------------

If the THOR run is already finished, you can also use the diagnostics
command like above with reduced information being collected.

Another possibility is to use the ``--run`` flag to rerun the last
THOR scan. In addition to conveniently rerunning the scan, THOR
Util can now watch over the THOR process for interrupting signals
from other processes (e.g. anti virus) which greatly helps in
determining if anti virus exclusions for THOR are applied correctly
or not. Using the ``--run`` flag should be the preferred method if
THOR is exiting unexpectedly.

.. code:: none

   thor-util.exe diagnostics --run
