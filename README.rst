Wagtail StreamForms
===================

|CircleCI| |Coverage Status|

This package is currently a concept but allows you to add add forms that
are built in the cms admin area to any streamfield. You can also create
your own form templates which will then appear as a template choice when
you build your form. This allows you to decide how the form is submitted
and to where.

Documentation is currently being worked on but the basics are below

Whats included?
---------------

-  Forms can be built in the cms admin and used site wide in any
   streamfield.
-  You can create your own form templates to display/submit how ever you
   wish to do it.
-  We have included a mixin which will handle the form post if it is
   being submitted to a wagtail page.
-  Forms are catagorised by their class in the cms admin for easier
   navigation.
-  Form submissions are also listed by their form which you can filter
   by date and are ordered by newest first.
-  Recaptcha can be added to a form.
-  You can also add site wide regex validators fo use in regex fields.

Screen shots
------------

.. figure:: https://github.com/AccentDesign/wagtailstreamforms/raw/master/images/screen1.png
   :alt: Screen1

.. figure:: https://github.com/AccentDesign/wagtailstreamforms/raw/master/images/screen2.png
   :alt: Screen2

.. figure:: https://github.com/AccentDesign/wagtailstreamforms/raw/master/images/screen3.png
   :alt: Screen3

.. figure:: https://github.com/AccentDesign/wagtailstreamforms/raw/master/images/screen4.png
   :alt: Screen4

.. figure:: https://github.com/AccentDesign/wagtailstreamforms/raw/master/images/screen5.png
   :alt: Screen5

Documentation
-------------

Can be found on `readthedocs <http://wagtailstreamforms.readthedocs.io/>`_.

Example site with docker
------------------------

Run the docker container

.. code:: bash

    $ docker-compose up

Create yourself a superuser

.. code:: bash

    $ docker exec -it <container_name> bash
    $ python manage.py createsuperuser

Go to http://127.0.0.1:8000

Testing
-------

Install dependencies

You will need pyenv installed see https://github.com/pyenv/pyenv

Also tox needs to be installed

.. code:: bash

    $ pip install tox

Install python versions in pyenv

.. code:: bash

    $ pyenv install 3.4.4
    $ pyenv install 3.5.3
    $ pyenv install 3.6.2

Set local project versions

.. code:: bash

    $ pyenv local 3.4.4 3.5.3 3.6.2

Run the tests

.. code:: bash

    $ tox

or run for a single environment

.. code:: bash

    $ tox -e py36-dj111-wt112

.. |CircleCI| image:: https://circleci.com/gh/AccentDesign/wagtailstreamforms/tree/master.svg?style=svg
   :target: https://circleci.com/gh/AccentDesign/wagtailstreamforms/tree/master
.. |Coverage Status| image:: https://coveralls.io/repos/github/AccentDesign/wagtailstreamforms/badge.svg?branch=master
   :target: https://coveralls.io/github/AccentDesign/wagtailstreamforms?branch=master