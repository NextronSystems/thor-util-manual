Log Conversion (logconvert)
===========================

The log conversion features allows you to convert THOR Logs between
different formats. You can chose whatever format fits your needs the most:

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
.. [2] The help menu shows the flag is existing, but this is not implemented yet.

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
  The feature to convert logs into CSV and CSV-zip was introduced in THOR Util
  Version 1.11.0

Conversion Examples
~~~~~~~~~~~~~~~~~~~

Here you can find some examples on how to convert logs to different formats.

Your command should always follow the same structure of a ``--from`` format,
as well as a ``--to`` format. Additionally, you also need to instruct which file
is your input file ``-f`` and which should be your output file ``-o``.

.. code:: console
 
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-json -f thor.txt -o thor-converted.json
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv -f thor.txt -o thor-converted.csv
   user@unix:~/thor$ ./thor-util logconvert --from-json --to-log -f thor.json -o thor-converted.log
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv -f thor.txt -o thor-converted.csv
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-csv-zip -f thor.txt -o thor-converted.zip
