RPA Framework
=============

.. contents:: Table of Contents
   :local:
   :depth: 1

.. include-marker

Introduction
------------

`RPA Framework` is a collection of open-source libraries and tools for
Robotic Process Automation (RPA), and it is designed to be used with both
`Robot Framework`_ and Python_. The goal is to offer well-documented and
actively maintained core libraries for Software Robot Developers.

Learn more about RPA at Robohub_.

**The project is:**

- 100% Open Source
- Sponsored by Robocorp_
- Optimized for Robocloud_ and Robocode_
- Accepting external contributions

.. _Robot Framework: https://robotframework.org
.. _Robot Framework Foundation: https://robotframework.org/foundation/
.. _Python: https://python.org
.. _Robohub: https://hub.robocorp.com
.. _Robocorp: https://robocorp.com
.. _Robocloud: https://hub.robocorp.com/introduction/robocorp-suite/robocloud/
.. _Robocode: https://hub.robocorp.com/introduction/robocorp-suite/robocode-lab/

Links
^^^^^

- Homepage: `<https://www.github.com/robocorp/rpaframework/>`_
- Documentation: `<https://rpaframework.org/>`_
- PyPI: `<https://pypi.org/project/rpaframework/>`_

------------

.. image:: https://github.com/robocorp/rpaframework/workflows/main/badge.svg
   :target: https://github.com/robocorp/rpaframework/actions?query=workflow%3Amain
   :alt: Status

.. image:: https://img.shields.io/pypi/v/rpaframework.svg?label=version
   :target: https://pypi.python.org/pypi/rpaframework
   :alt: Latest version

.. image:: https://img.shields.io/pypi/l/rpaframework.svg
   :target: http://www.apache.org/licenses/LICENSE-2.0.html
   :alt: License


Libraries
---------

The RPA Framework project currently includes the following libraries:

+----------------------------+----------------------------------------------+
| `Browser`_                 | Control browsers and automate the web        |
+----------------------------+----------------------------------------------+
| `Cloud.AWS`_               | Use Amazon AWS services                      |
+----------------------------+----------------------------------------------+
| `Cloud.Azure`_             | Use Microsoft Azure services                 |
+----------------------------+----------------------------------------------+
| `Cloud.Google`_            | Use Google Cloud services                    |
+----------------------------+----------------------------------------------+
| `Database`_                | Interact with databases                      |
+----------------------------+----------------------------------------------+
| `Desktop.Clipboard`_       | Interact with the system clipboard           |
+----------------------------+----------------------------------------------+
| `Desktop.OperatingSystem`_ | Read OS information and manipulate processes |
+----------------------------+----------------------------------------------+
| `Desktop.Windows`_         | Automate Windows desktop applications        |
+----------------------------+----------------------------------------------+
| `Email.Exchange`_          | E-Mail operations (Exchange protocol)        |
+----------------------------+----------------------------------------------+
| `Email.ImapSmtp`_          | E-Mail operations (IMAP & SMTP)              |
+----------------------------+----------------------------------------------+
| `Excel.Application`_       | Control the Excel desktop application        |
+----------------------------+----------------------------------------------+
| `Excel.Files`_             | Manipulate Excel files directly              |
+----------------------------+----------------------------------------------+
| `FileSystem`_              | Read and manipulate files and paths          |
+----------------------------+----------------------------------------------+
| `FTP`_                     | Interact with FTP server                     |
+----------------------------+----------------------------------------------+
| `HTTP`_                    | Interact directly with web APIs              |
+----------------------------+----------------------------------------------+
| `Images`_                  | Manipulate images                            |
+----------------------------+----------------------------------------------+
| `Notifier`_                | Notify messages using different services     |
+----------------------------+----------------------------------------------+
| `Outlook.Application`_     | Control the Outlook desktop application      |
+----------------------------+----------------------------------------------+
| `PDF`_                     | Read and create PDF documents                |
+----------------------------+----------------------------------------------+
| `Robocloud.Items`_         | Use the Robocloud Work Items API             |
+----------------------------+----------------------------------------------+
| `Robocloud.Secrets`_       | Use the Robocloud Secrets API                |
+----------------------------+----------------------------------------------+
| `Salesforce`_              | Salesforce operations                        |
+----------------------------+----------------------------------------------+
| `SAP`_                     | Control SAP GUI desktop client               |
+----------------------------+----------------------------------------------+
| `Slack`_                   | Send notifications to Slack channels         |
+----------------------------+----------------------------------------------+
| `Tables`_                  | Manipulate, sort, and filter tabular data    |
+----------------------------+----------------------------------------------+
| `Tasks`_                   | Control task execution                       |
+----------------------------+----------------------------------------------+
| `Twitter`_                 | Twitter API interface                        |
+----------------------------+----------------------------------------------+
| `Word.Application`_        | Control the Word desktop application         |
+----------------------------+----------------------------------------------+

.. _Browser: https://rpaframework.org/libraries/browser/
.. _Cloud.AWS: https://rpaframework.org/libraries/cloud_aws/
.. _Cloud.Azure: https://rpaframework.org/libraries/cloud_azure/
.. _Cloud.Google: https://rpaframework.org/libraries/cloud_google/
.. _Database: https://rpaframework.org/libraries/database/
.. _Desktop.Clipboard: https://rpaframework.org/libraries/desktop_clipboard/
.. _Desktop.Operatingsystem: https://rpaframework.org/libraries/desktop_operatingsystem/
.. _Desktop.Windows: https://rpaframework.org/libraries/desktop_windows/
.. _Email.Exchange: https://rpaframework.org/libraries/email_exchange/
.. _Email.ImapSmtp: https://rpaframework.org/libraries/email_imapsmtp/
.. _Excel.Application: https://rpaframework.org/libraries/excel_application/
.. _Excel.Files: https://rpaframework.org/libraries/excel_files/
.. _FileSystem: https://rpaframework.org/libraries/filesystem/
.. _FTP: https://rpaframework.org/libraries/ftp/
.. _HTTP: https://rpaframework.org/libraries/http/
.. _Images: https://rpaframework.org/libraries/images/
.. _Notifier: https://rpaframework.org/libraries/notifier/
.. _Outlook.Application: https://rpaframework.org/libraries/outlook_application/
.. _PDF: https://rpaframework.org/libraries/pdf/
.. _Robocloud.Items: https://rpaframework.org/libraries/robocloud_items/
.. _Robocloud.Secrets: https://rpaframework.org/libraries/robocloud_secrets/
.. _Salesforce: https://rpaframework.org/libraries/salesforce/
.. _SAP: https://rpaframework.org/libraries/sap/
.. _Slack: https://rpaframework.org/libraries/slack/
.. _Tables: https://rpaframework.org/libraries/tables/
.. _Tasks: https://rpaframework.org/libraries/tasks/
.. _Twitter: https://rpaframework.org/libraries/twitter/
.. _Word.Application: https://rpaframework.org/libraries/word_application/


Installation
------------

If you already have Python_ and `pip <http://pip-installer.org>`_ installed,
you can use:

``pip install rpaframework``

.. note:: Python 3.6 or higher is required

Example
-------

After installation the libraries can be directly imported inside
`Robot Framework`_:

.. code:: robotframework

    *** Settings ***
    Library    RPA.Browser

    *** Tasks ***
    Login as user
        Open browser  https://example.com
        Input text    id:user-name    ${USERNAME}
        Input text    id:password     ${PASSWORD}

The libraries are also available inside Python_:

.. code:: python

    from RPA.Browser import Browser

    lib = Browser()

    lib.open_browser("https://example.com")
    lib.input_text("id:user-name", username)
    lib.input_text("id:password", password)

Support and contact
-------------------

- `rpaframework.org <https://rpaframework.org/>`_ for library documentation
- Robohub_ for guides and tutorials
- **#rpaframework** channel in `Robot Framework Slack`_ if you
  have open questions or want to contribute

.. _Robot Framework Slack: https://robotframework-slack-invite.herokuapp.com/

Contributing
------------

Found a bug? Missing a critical feature? Interested in contributing?
Head over to the `Contribution guide <https://rpaframework.org/contributing/guide.html>`_
to see where to get started.

License
-------

This project is open-source and licensed under the terms of the
`Apache License 2.0 <http://apache.org/licenses/LICENSE-2.0>`_.
