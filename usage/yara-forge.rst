YARA Forge
===========

YARA-Forge (https://yarahq.github.io/) is an open source project that
bundles YARA rules from different open source projects. Rules are offered
in different **rulesets** that differ in their FP ratio / detection rate tradeoff.

THOR Util offers support for downloading YARA Forge with:

.. code:: doscon
 
   C:\thor>thor-util.exe yara-forge download --ruleset <ruleset>

Where **ruleset** can be one of the following:

- core
- extended
- full

.. note::
   Only one ruleset at a time can be used. When you download a new
   ruleset, the old one gets overwritten.

A downloaded YARA Forge ruleset is stored in ``custom-signatures/yara-forge``
and is automatically updated with ``thor-util update``.

If you no longer want to use YARA Forge, you can run:

.. code:: doscon
 
   C:\thor>thor-util.exe yara-forge remove
