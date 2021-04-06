.. role:: raw-html-m2r(raw)
   :format: html

Custom Signature Encryption (encrypt)
=====================================

You can encrypt the YARA signatures and IOC files with the help of
THOR-Util’s “encrypt” feature.

.. code:: batch
   
   thor-util.exe encrypt --help

.. figure:: ../images/image4.png
   :target: ../_images/image4.png
   :alt: THOR Util's Encrypt Feature Help
  
   THOR Util's Encrypt Feature Help

As target for the encrypt command, you can use a single file, a list of
files or wildcards.

.. code:: batch 
 
   thor-util.exe encrypt ~/sigs/case14.yar                                                                
   thor-util.exe encrypt ~/sigs/case14.yar ~/sigs/case14-hashes.txt
   thor-util.exe encrypt ~/sigs/case14.\*

It will automatically detect the type of the signature based on its
extension.

+--------------------+-------------------------------------+-------------------------------+
| File Type          | Clear Text Extension                | Extension of Encrypted File   |
+====================+=====================================+===============================+
| IOC File           | .txt                                | .dat                          |
+--------------------+-------------------------------------+-------------------------------+
| YARA Rule          | .yar, .yara, .yac (compiled YARA)   | .yas                          |
+--------------------+-------------------------------------+-------------------------------+
| Sigma              | .yml, .yaml                         | .yms                          |
+--------------------+-------------------------------------+-------------------------------+
| STIXv2             | .json                               | .jsos                         |
+--------------------+-------------------------------------+-------------------------------+

Place the encrypted IOC files in the “./custom-signatures” sub folder in
the program directory and the encrypted YARA rules in the
“./custom-signatures/yara” sub folder.
