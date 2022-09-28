===========
Description
===========
Detect package carrier from tracking number and generate tracking url.

============
Requirements
============
* python >= 3.4

============
Installation
============
.. code-block:: bash

    $ pip install tracking_url

=====
Usage
=====

.. code-block:: python

    import tracking_url

    match = tracking_url.guess_carrier('0123456789')
    if match is None:
        print('No matching carrier found')
    else:
        print('Number:', match.number)
        print('Carrier:', match.carrier)
        print('Url:', match.url)

=======================
How to Make New Release
=======================
Update version in ``version.py`` by changing the last number to be one greater.
Example, change

.. code-block:: python

    __version__ = "v0.0.5+d2d.003"

to

.. code-block:: python

    __version__ = "v0.0.5+d2d.004"

Commit and push changes, then go to https://github.com/Draft2Digital/tracking-url/releases
and click **Draft a new release**.

Click **Choose a tag** and put in the same version as is the value in the ``__version__`` variable (e.g. ``v0.0.5+d2d.004``).
Publish the release. In projects that use this, update the version pointed at to be the new version.

======
Thanks
======
This code is a simple python port of the identically named node module.

Big thanks to https://github.com/wankdanker for the original code and
research.

======
Issues
======
If you have any suggestions, bug reports or annoyances please report them
to the issue tracker at https://github.com/sereema/tracking-url/issues .
