README
======

Description
-----------

This Repository is for building Sphinx Documentation to be published to github.io. The publishing process is handled automatically via Github Actions when a change is merged into the main branch of this Repository. 

The documentation can be viewed at https://jared-bloomer.github.io/KW4JLB-Documentation/

Building Locally
----------------

To build this site locally use the ``Makefile`` in ``docs/``.

.. code-block:: bash

    cd docs
    make html

The files will be located in docs/build/ and you can open the index.html in your browser to preview changes before publishing them. 

