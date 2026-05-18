Log Conversion (logconvert)
===========================

The log conversion feature allows you to convert THOR logs between
different formats. Choose the format that fits your needs:

.. list-table:: 
   :header-rows: 1

   * - Format
     - Convert From
     - Convert To
   * - **Log** [1]_
     - Yes
     - Yes
   * - **JSON**
     - Yes
     - Yes
   * - **Key-Value**
     - No [2]_
     - Yes
   * - **CSV**
     - No
     - Yes
   * - **ZIP CSV**
     - No
     - Yes

.. [1] This is the default THOR log format ``<hostname>_timestamp.txt``.
.. [2] The help menu shows this flag, but the function is not implemented yet.

.. code-block:: doscon

   C:\nextron\thor>thor-util.exe logconvert --help
       ________ ______  ___    __  ______________
      /_  __/ // / __ \/ _ \  / / / /_  __/  _/ /
       / / / _  / /_/ / , _/ / /_/ / / / _/ // /__
      /_/ /_//_/\____/_/|_|  \____/ /_/ /___/____/

      Copyright by Nextron Systems GmbH, 2023
      v1.11.0+thor10.7.6

   Convert log file into another format

   Usage:
     thor-util logconvert [flags]

   Examples:
     thor-util logconvert --from-json --to-log --file example.json --output example.log

   Flags:
     -f, --file string     Input file
         --from-json       Convert from JSON
         --from-kv         Convert from KV
         --from-log        Convert from Log
     -h, --help            help for logconvert
     -o, --output string   Output file
         --to-csv          Convert to CSV
         --to-csv-zip      Convert to ZIP containing one CSV log per module
         --to-json         Convert to JSON
         --to-kv           Convert to KV
         --to-log          Convert to Log

.. note:: 
  The feature to convert logs into CSV and ZIP CSV was introduced in THOR Util
  version 1.11.0.

Conversion Examples
~~~~~~~~~~~~~~~~~~~

The following examples show how to convert logs to different formats.

Each command uses the same structure: a ``--from`` format, a ``--to``
format, an input file with ``-f``, and an output file with ``-o``.

.. code:: console
 
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-json -f thor.txt -o thor-converted.json
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv -f thor.txt -o thor-converted.csv
   user@unix:~/thor$ ./thor-util logconvert --from-json --to-log -f thor.json -o thor-converted.log
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv -f thor.txt -o thor-converted.csv
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv-zip -f thor.txt -o thor-converted.zip
