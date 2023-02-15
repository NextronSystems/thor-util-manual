Log Conversion (logconvert)
===========================

The log conversion features allows to convert between Text and JSON
format.

.. figure:: ../images/image11.png
   :target: ../_images/image11.png
   :alt: Log Conversion Options

   Log Conversion Options

.. code:: console
 
   user@unix:~/thor$ ./thor-util logconvert --from-log --to-json -f thor.log -o thor-converted.json
   user@unix:~/thor$ ./thor-util logconvert --from-json --to-log -f thor.json -o thor-converted.log
