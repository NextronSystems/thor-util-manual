Log Conversion (logconvert)
===========================

The log conversion features allows to convert between Text and JSON
format.

.. figure:: ../images/image11.png
   :target: ../_images/image11.png
   :alt: Log Conversion Options

   Log Conversion Options

.. code:: bash
 
   ./thor-util logconvert --from-log --to-json -f thor.log -o thor-converted.json
   ./thor-util logconvert --from-json --to-log -f thor.json -o thor-converted.log
