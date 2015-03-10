Welcome to aiopyramid's documentation!
======================================

A library for leveraging pyramid infrastructure asynchronously using the new :mod:`asyncio`.

``Aiopyramid`` provides tools for making web applications with :ref:`Pyramid <pyramid:index>` and :mod:`asyncio`.
It will not necessarily make your application run faster. Instead, it gives you some tools
and patterns to build an application on asynchronous servers.
Bear in mind that you will need to use asynchronous libraries for io where appropriate.

This is not a fork of :ref:`Pyramid <pyramid:index>` and it does not rewrite
any :ref:`Pyramid <pyramid:index>` code to run asynchronously!
:ref:`Pyramid <pyramid:index>` is just that flexible.

Since this library is built on relatively new technology, it is not intended for production use.

Getting Started
---------------

``Aiopyramid`` includes a scaffold that creates a "hello world" application,
check it out! The scaffold is designed to work with either `gunicorn`_
via a custom worker or `uWSGI`_ via the `uWSGI asyncio plugin`_.

For example:

::

    pip install aiopyramid gunicorn
    pcreate -s aio_starter <project>
    cd <project>
    python setup.py develop
    gunicorn --paste development.ini

There is also a :term:`websocket` scaffold `aio_websocket` with basic tools for setting up
a :term:`websocket` server.

For a more detailed walkthrough of how to setup ``Aiopyramid`` see the :doc:`tutorial/index`.


Contents
--------

.. toctree::
    :maxdepth: 3

    tutorial/index
    features
    websockets
    servers
    tests
    approach


Contributors
------------

- Jason Housley
- Guillaume Gauvrit
- Tiago Requeijo
- Ander Ustarroz

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
* :doc:`glossary`

.. _gunicorn: http://gunicorn.org
.. _uWSGI: https://github.com/unbit/uwsgi
.. _uWSGI asyncio plugin: http://uwsgi-docs.readthedocs.org/en/latest/asyncio.html
