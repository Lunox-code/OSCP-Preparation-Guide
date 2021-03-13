Immunity Debugger
=================

**Always run Immunity Debugger as Administrator if you can.**

There are generally two ways to use Immunity Debugger to debug an application:

1. Make sure the application is running, open Immunity Debugger, and then use :code:`File -> Attach` to attack the debugger to the running process.
2. Open Immunity Debugger, and then use :code:`File -> Open` to run the application.

When attaching to an application or opening an application in Immunity Debugger, the application will be paused. Click the "Run" button or press F9.

Note: If the binary you are debugging is a Windows service, you may need to restart the application via :code:`sc`

.. code-block:: none

    sc stop SLmail
    sc start SLmail

Some applications are configured to be started from the service manager and will not work unless started by service control.

Mona Setup
==========

Mona is a powerful plugin for Immunity Debugger that makes exploiting buffer overflows much easier.

| The latest version can be downloaded here: https://github.com/corelan/mona
| The manual can be found here: https://www.corelan.be/index.php/2011/07/14/mona-py-the-manual/

Copy the mona.py file into the PyCommands directory of Immunity Debugger (usually located at C:\\Program Files\\Immunity Inc\\Immunity Debugger\\PyCommands).

In Immunity Debugger, type the following to set a working directory for mona.

.. code-block:: none

    !mona config -set workingfolder c:\mona\%p

Keeping mona.py up-to-date
==========================
.. code-block:: none

    !mona update
