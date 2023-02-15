.. role:: raw-html-m2r(raw)
   :format: html

Templates
===========================

THOR Util reads a default configuration from ``config/thor-util.yml``.

Within this file, default parameters can be set in YAML form.

These default parameters can be overridden with command line flags.

All global flags for THOR Util are supported in the configuration file.
These flags can be shown with:

.. code:: console
 
   user@unix:~/thor$ ./thor-util --help

Proxy configuration
-------------------

If you want to use a specific HTTP proxy, this can be
specified in your configuration file with:

.. code:: yaml

   proxy: http://myproxy:8080

TechPreview configuration
--------------------------

If you always want to download the latest TechPreview instead of
the standard THOR version, add:

.. code:: yaml

   techpreview: True
