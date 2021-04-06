.. role:: raw-html-m2r(raw)
   :format: html

Upgrade (upgrade) and Updates (update)
======================================

You can download updates for THOR and SPARK with “thor-util.exe”
(Windows) or “thor-util” (Linux, macOS).

Running “thor-util --help” shows three options that seem to have a very
similar meaning: “upgrade”, “update” and “download”.

The difference is that the “download” option downloads a full pack with
all config files while the “upgrade” option fetches a full package but
excludes the config files to avoid accidental overwrites of local config
files (like: thor.yml, falsepositive\_filters.cfg etc.).

The “update” option only works with THOR 10 and retrieves only the
newest signature pack.

+------------+------------------------------------------------------+--------------------------+
| Option     | ­­­Description                                       | Program                  |
+============+======================================================+==========================+
| upgrade    | Get new program files and signatures                 | THOR 8, SPARK, THOR 10   |
+------------+------------------------------------------------------+--------------------------+
| update     | Get new signatures                                   | THOR 10                  |
+------------+------------------------------------------------------+--------------------------+
| download   | Get new program files, signatures and config files   | THOR 8, SPARK, THOR 10   |
+------------+------------------------------------------------------+--------------------------+

If you have a full program package present, you should use the “upgrade”
option.

Every other option has its own help. You can see the help of each option
with

.. code:: bash
   
   thor-util *option* --help

.. figure:: ../images/image2.png
   :target: ../_images/image2.png
   :alt: THOR Util Upgrade Help

   THOR-util Upgrade Help

The following two examples show different upgrade methods.

.. code:: batch
   
   thor-util.exe upgrade
   thor-util.exe upgrade -a https://proxy.company.net:8080
   thor-util.exe upgrade -a https://proxy.company.net:8080 -n dom\\user -p password
   thor-util.exe upgrade -a https://proxy.local:8080 --ntlm -n dom\\user -p password

THOR TechPreview Version
------------------------

To download the unstable TechPreview version, use the following command
line flag.

.. code:: batch
   
   thor-util.exe upgrade --techpreview 

Update Locations
----------------

The following servers are used as update mirrors and should be
accessible via HTTPS:

update1.nextron-systems.com

update2.nextron-systems.com

Update Server Information
-------------------------

You can get information on the available update packages on this site:

https://update1.nextron-systems.com/info.php

.. figure:: ../images/image3.png
   :target: ../_images/image3.png
   :alt: Update server information

   Update server information
