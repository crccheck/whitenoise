WhiteNoise
==========

.. image:: https://travis-ci.org/evansd/whitenoise.png
   :target:  https://travis-ci.org/evansd/whitenoise
   :alt: Build Status

.. image:: https://badge.fury.io/py/whitenoise.png
    :target: https://pypi.python.org/pypi/whitenoise
    :alt: Latest PyPI version

WSGI middleware for easy serving of static files, with optional integration with Django.
Secure and efficient enough to use in production, and designed to be CDN-friendly for
high-traffic sites.

Just wrap your WSGI application in the WhiteNoise middleware, give it the path to your
static files directory and any requests matching files in that directory will be served
correctly. All other requests are passed on to your application.

Features
--------

 * Simple to configure
 * Handles caching (sends cache headers and returns Not Modified responses when appropriate)
 * Serves gzipped content (handling Accept-Encoding and Vary headers correctly)
 * Provides hooks for customisation, e.g. sending custom headers for certain files
 * Can serve static files from arbitrary URLs, not just from a fixed URL prefix, so
   you can use it to serve files like ``/favicon.ico`` or ``/robots.txt``
 * Django version can automatically gzip your files, create uniquely-named versions of each
   file and set them to be cached forever -- all with one line of config

Documentation
-------------

 * Main documentation site: `<http://whitenoise.evans.io>`_
 * Get started with `WhiteNoise and Django <http://whitenoise.evans.io/en/latest/django.html>`_
 * Get started with `WhiteNoise and any other WSGI application <http://whitenoise.evans.io/en/latest/base.html>`_

Shouldn't I be using a real webserver, or a CDN, or Amazon S3?
See `Infrequently Asked Questions <http://whitenoise.evans.io/en/latest/ifaqs.html>`_


Compatibility
-------------

WhiteNoise works with any WSGI-compatible application and is tested on Python **2.7**, **3.3** and **3.4**

DjangoWhiteNoise is tested with Django versions **1.4** --- **1.7**


Endorsements
------------

WhiteNoise is being used in `Warehouse <https://github.com/pypa/warehouse>`_, the in-development
replacement for the PyPI package repository.

Some of Django and pip's core developers have said nice things about it:

   `@jezdez <https://twitter.com/jezdez/status/440901769821179904>`_: "*[WhiteNoise]
   is really awesome and should be the standard for Django + Heroku*"

   `@dstufft <https://twitter.com/dstufft/status/440948000782032897>`_: "*Whitenoise
   looks pretty excellent.*"


Issues
------

See the `GitHub issue tracker <https://github.com/evansd/whitenoise/issues>`_.


License
-------

MIT Licensed
