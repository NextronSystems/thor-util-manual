Download Packages (download)
============================

Use the "download" command to download scanner packages for Windows,
Linux, and macOS.

.. note:: 
   THOR Util cannot download THOR binaries and signatures whose license
   was obtained through the Management Center. Use the Management Center
   API for these downloads. THOR Util only accepts the Nextron Customer
   Portal as a license source.

This option is useful when you need to download updates on an
Internet-connected machine and transfer them to a system without Internet
access.

.. code:: doscon
 
   C:\thor>thor-util.exe download -t thor10-win

THOR TechPreview Version
------------------------

To download the TechPreview version, use the following command-line flag:

.. code:: doscon
   
   C:\thor>thor-util.exe download -t thor10-win --techpreview

You can find more information on the TechPreview version
`here <https://www.nextron-systems.com/2020/08/31/introduction-thor-techpreview/>`_.
