.. role:: raw-html-m2r(raw)
   :format: html

Log Conversion (logconvert)
===========================

The log conversion features allows to convert between Text and JSON
format.

.. figure:: ../images/image11.png
   :target: ../_images/image11.png
   :alt: Log Conversion Options

   Log Conversion Options

.. code::bash
 
   ./thor-util logconvert --from-log --to-json -f spark.log -o spark-converted.json
   ./thor-util logconvert --from-json --to-log -f spark.json -o spark-converted.log
