
*******************************
How I set up my school printers
*******************************

:date: 11 May 2015

I use Ubuntu 14.04 on my personal laptop at the moment. Here is how I add the printers.

#. Go to *System Settings*, then *Printers*, or open *Printers* from the Launcher.
#. Click Add.
#. Choose the printer you want from the `printer list`_. Say you choose ``dali``.
#. In the *New Printer* dialog, click *Network Printer → Windows Printer via SAMBA*. Add a printer from the URL ``smb://socs-ad/sms-2.cs.bham.ac.uk/dali``.
   
   Use *Set authentication details now*, using your School username + password. Do not try *Verify...*, it will not work, but printing will work.

#. In the driver selection dialog, choose the recommended driver, and use the options recommended by the School. You can find these by clicking on the printer types in the `printer list`_.
#. For both the printer name and description, use the printer name like ``dali``. Copy the room number from the printer list to the *Location* field if you want.
#. Print a test page.
   
If you ``ssh`` to a School server, you can test if the printing worked, by running e.g. ``lpq -P dali`` repeatedly. Or run it in a loop with ``watch -n .5 lpq -P dali``. Or, of course, you can actually walk to the printer.

The printers I add like this work on my personal laptop, but only if I connect from the wired network. The wireless network is separate in some ways and printing won't work; you might have luck using the VPN, or you can ``scp`` your PDFs to a School machine and ``lpr`` with the correct options from there. The ``scp`` approach works, but it's really not as handy as just setting up printers the normal way.
   
This guide is based on the School guide for `printing on self maintained Windows PCs`_.

.. _printer list: http://supportweb.cs.bham.ac.uk/printing/printers.php
.. _printing on self maintained Windows PCs: http://supportweb.cs.bham.ac.uk/printing/non_domain.php