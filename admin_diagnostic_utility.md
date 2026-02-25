.. \_admin\_diagnostic\_utility:

Diagnostic tool
===============================

Starting from version 2.1, the installation package includes diagnostic tool sdc-tantor.

It is to be used in case of installation or Platform update failure.


.. important::

   If there is no execution flag in the file attributes, install it using the following command:

   .. code-block:: bash

      # chmod 755 ./sdc-tantor

Command to execute the utility:

.. code-block:: bash

   \# ./sdc-tantor

Command input result:

   ::

      SDC-Tantor (version 1.0.0)
      System configuration data and diagnostic information will be collected
      from this OS.
      ...

Message in the console about the completion of the diagnostic procedure:

   ::

      Data collection completed.
      Creating archive..
      Archive created and saved in:
            sdc-report_test-01.tantorlabs.ru_20230718_194100.tar.gz
      Please attach this file to the support ticket.
      #

