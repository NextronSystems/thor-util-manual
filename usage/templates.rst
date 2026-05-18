Templates
===========================

THOR Util reads a default configuration from ``config/thor-util.yml``.

Use this file to set default parameters in YAML format.

Command-line flags override these default parameters.

All global flags for THOR Util are supported in the configuration file.
You can view these flags with:

.. code:: console
 
   user@unix:~/thor$ ./thor-util --help

Proxy configuration
-------------------

To use a specific HTTP proxy, add it to your configuration file:

.. code:: yaml

   proxy: http://myproxy:8080

TechPreview configuration
-------------------------

To always download the latest TechPreview instead of the standard THOR
version, add:

.. code:: yaml

   techpreview: True
