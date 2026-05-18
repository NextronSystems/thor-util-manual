Verify Binaries (verify)
========================

Use the "verify" command to verify the authenticity of the included
binaries. Signature verification is based on a public key encryption
algorithm and requires the ``*.sig`` files shipped with the packages.

.. figure:: ../images/thor-util-verify-thor.exe
   :alt: Verify thor.exe signature using THOR Util

   Verify thor.exe signature using THOR Util

To verify the integrity of THOR Util, download the public key from
Nextron's website: https://www.nextron-systems.com/pki/
You can then use the public key with the following commands to verify
``thor-util``:

On Windows:

.. code:: doscon

   C:\thor>openssl dgst -sha256 -verify codesign.pem -signature thor-util.exe.sig thor-util.exe

On Linux:

.. code:: console

   C:\thor>openssl dgst -sha256 -verify codesign.pem -signature thor-util.sig thor-util
