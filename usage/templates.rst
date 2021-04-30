.. role:: raw-html-m2r(raw)
   :format: html

Templates
===========================

THOR Util reads a default configuration from `config/thor-util.yml`.

Within this file, parameters can be set in YAML form:
Say, for example, that you always want to use an HTTP proxy. This can be
specified in your configuration file with:

.. code:: batch

   proxy: http://myproxy:8080

These default parameters can be overridden with command line flags.

All global flags for THOR Util are supported in the configuration file.
These flags can be shown with:

.. code:: batch
 
   ./thor-util --help
