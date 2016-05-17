Eckerd Django Google SSO
============

A reusable django application for google sso

Installation
------------

To get the latest stable release from PyPi

.. code-block:: bash

    pip install eckerd-django-google-sso

To get the latest commit from GitHub

.. code-block:: bash

    pip install -e git+git://github.com/christopherdavenport/eckerd-django-google-sso.git#egg=eckerd-django-google-sso

TODO: Describe further installation steps (edit / remove the examples below):

Add ``eckerd-django-google-sso`` to your ``INSTALLED_APPS``

.. code-block:: python

    INSTALLED_APPS = (
        ...,
        'eckerd-django-google-sso',
    )

Add the ``eckerd-django-google-sso`` URLs to your ``urls.py``

.. code-block:: python

    urlpatterns = [
        url(r'^/', include('eckerd-django-google-sso.urls')),
    ]

Before your tags/filters are available in your templates, load them by using

.. code-block:: html

	{% load backend_utils %}


Don't forget to migrate your database

.. code-block:: bash

    ./manage.py migrate eckerd-django-google-sso


Usage
-----

TODO: Describe usage or point to docs. Also describe available settings and
templatetags.


Contribute
----------

If you want to contribute to this project, please perform the following steps

.. code-block:: bash

    # Fork this repository
    # Clone your fork
    mkvirtualenv -p python2.7 eckerd-django-google-sso
    make develop

    git co -b feature_branch master
    # Implement your feature and tests
    git add . && git commit
    git push -u origin feature_branch
    # Send us a pull request for your feature branch

In order to run the tests, simply execute ``tox``. This will install two new
environments (for Django 1.8 and Django 1.9) and run the tests against both
environments.
