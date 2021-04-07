.. role:: raw-html-m2r(raw)
   :format: html

License Retrieval (license)
===========================

This feature can be used to retrieve a license from a remote ASGARD
server system.

.. figure:: ../images/image8.png
   :target: ../_images/image8.png
   :alt: THOR Util's license generation feature

   THOR Util's license generation feature

.. figure:: ../images/image9.png
   :target: ../_images/image9.png
   :alt: License retrieval from an ASGARD server

   License retrieval from an ASGARD server

.. code:: bash
 
   thor-util license --hostname machine1 server --url https://asgard1.bsk
   thor-util license --http-insecure --url https://asgard1.bsk
