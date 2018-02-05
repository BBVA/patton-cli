Patton-cli - The knife of the Admin & Security auditor
======================================================

+----------------+-----------------------------------------------+
|Current version | 0.0.1                                         |
+----------------+-----------------------------------------------+
|Project site    | https://github.com/bbva/patton-client         |
+----------------+-----------------------------------------------+
|Issues          | https://github.com/bbva/patton-client/issues/ |
+----------------+-----------------------------------------------+
|Python versions | 3.6 or above                                  |
+----------------+-----------------------------------------------+

What's Patton cli?
==================

Patton-cli (*P*atton-*C*li) born with the objective to be a knife for system admins and security auditors.

PC could be filled with many different sources and can report results in many formats, being great for scripting.

Installation
============

Install Patton is easy:

.. code-block:: bash

    > python3.6 -m pip install patton-cli


.. note::

    Patton-cli need a `Patton-server <https://github.com/BBVA/patton-server>`_. Be sure that the server are running!

Getting started
===============

Quick example
-------------

.. code-block:: bash

    > patton django:1.9

    +------------+-------------------------------------+---------------------+
    | Name       | CPEs                                | CVEs                |
    +------------+-------------------------------------+---------------------+
    | django:1.9 | cpe:/a:djangoproject:django:1.9:rc2 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc2 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc2 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc2 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc1 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc1 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc1 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:rc1 | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:b1  | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    |            | ----------------------------------- | ------------------- |
    |            | cpe:/a:djangoproject:django:1.9:b1  | CVE-2017-7234 (5.8) |
    |            |                                     | ------------------- |
    |            |                                     | CVE-2017-7233 (5.8) |
    +------------+-------------------------------------+---------------------+


Getting help
------------

Patton-cli has self-explained doc:

.. code-block:: bash

    > patton -h

    usage: patton [-h] [-v] [--patton-host PATTON_HOST] [-F {table,json,csv}] [-q]
              [-i FROM_FILE] [-o OUTPUT_FILE]
              [-e {python,alpine,simple_parser,auto,nmap,dpkg}] [-s] [-D] [-B]
              [-t {auto,nmap}] [-f]
              [INPUT_LIST [INPUT_LIST ...]]

    Patton cli

    positional arguments:
      INPUT_LIST

    optional arguments:
      -h, --help            show this help message and exit
      -v                    log level
      --patton-host PATTON_HOST
                            patton server host
      -F {table,json,csv}, --display-format {table,json,csv}
                            display format options
      -q, --quiet           do not display any information in stdout
      -i FROM_FILE, --from-file FROM_FILE
                            output file for results
      -o OUTPUT_FILE, --output-file OUTPUT_FILE
                            results file. formats: csv, json, raw
      -e {python,alpine,simple_parser,auto,nmap,dpkg}, --source-type {python,alpine,simple_parser,auto,nmap,dpkg}
                            use specific source parser
      -s, --skip-on-fail    doesn't abort execution on dependency check fail

    Working modes:
      -D, --dependency      check libraries and versions (default)
      -B, --banner          check banners (currently experimental)

    Specific option for banners:
      -t {auto,nmap}, --banner-type {auto,nmap}
                            http, ftp, ...-
      -f, --follow          read from stdin and do a continuously check

    Examples:

      * Checking specific library and output as table:
        > patton django:1.2 flask:1.1.0

      * Checking Python installed dependencies and output as CSV:
        > pip freeze | patton -F csv
        or
        > patton -F csv -i requirements.txt

      * Checking ubuntu dependencies display as table and dump in json file:
        > dpkg -l | patton -e dpkg -F table -o results.json



Usage examples
==============

Getting vulnerabilities from different sources
----------------------------------------------

From Ubuntu
+++++++++++

.. code-block:: bash

    > dpkg -l | patton -e dpkg

From Brew
+++++++++

.. code-block:: bash

    > brew list --versions | patton

From Alpine
+++++++++++

.. code-block:: bash

    > apk version -v | patton -e alpine

From python requirements
++++++++++++++++++++++++

.. code-block:: bash

    > pip freeze | patton -e python

or

.. code-block:: bash

    > cat requirements.txt | patton -e python

or

.. code-block:: bash

    > patton -i requirements.txt -e python

Formatting the output
---------------------

Patton-cli can display results in these formats:

- Table
- JSON
- CSV

.. code-block:: bash

    > cat requirements.txt | patton -e python -F csv

.. code-block:: bash

    > cat requirements.txt | patton -e python -F json

.. code-block:: bash

    > cat requirements.txt | patton -e python -F table

Exporting results
-----------------

Patton-cli can export the results in format:

- Raw (table)
- JSON
- CSV

The format of file is determined by the extension:

.. code-block:: bash

    > cat requirements.txt | patton -e python -o report.json

.. code-block:: bash

    > cat requirements.txt | patton -e python -o report.csv

.. code-block:: bash

    > cat requirements.txt | patton -e python -o report.raw

Quiet mode
----------

If you don't want that Patton-cli reports anything by the terminal, you can use ::samp:`-q` option:


.. code-block:: bash

    > cat requirements.txt | patton -e python -q -o report.csv

Some funny examples
-------------------

Listing dependencies and check te vulns:

.. code-block:: bash

    > dpkg -l | tee patton -e dpkg -q -o reports.csv

Finding critical vulnerabilities:

.. code-block:: bash

    > dpkg -l | patton -e dpkg -F csv | grep "10\.0" > critial_vulns.txt


Contributing
============

Any collaboration is welcome!

There're many tasks to do.You can check the `Issues <https://github.com/bbva/patton-cli/issues/>`_ and send us a Pull Request.

Also you can read the `TODO <https://github.com/bbva/patton-cli/blob/master/TODO.md>`_ file.

License
=======

This project is distributed under `Apache 2 license <https://github.com/bbva/patton-cli/blob/master/LICENSE>`_
