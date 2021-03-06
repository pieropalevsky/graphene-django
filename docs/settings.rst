Settings
========

Graphene-Django can be customised using settings. This page explains each setting and their defaults.

Usage
-----

Add settings to your Django project by creating a Dictonary with name ``GRAPHENE`` in the project's ``settings.py``:

.. code:: python

    GRAPHENE = {
        ...
    }


``SCHEMA``
----------

The location of the top-level ``Schema`` class.

Default: ``None``

.. code:: python

    GRAPHENE = {
        'SCHEMA': 'path.to.schema.schema',
    }


``SCHEMA_OUTPUT``
-----------------

The name of the file where the GraphQL schema output will go.

Default: ``schema.json``

.. code:: python

    GRAPHENE = {
        'SCHEMA_OUTPUT': 'schema.json',
    }


``SCHEMA_INDENT``
-----------------

The indentation level of the schema output.

Default: ``2``

.. code:: python

    GRAPHENE = {
        'SCHEMA_INDENT': 2,
    }


``MIDDLEWARE``
--------------

A tuple of middleware that will be executed for each GraphQL query.

See the `middleware documentation <https://docs.graphene-python.org/en/latest/execution/middleware/>`__ for more information.

Default: ``()``

.. code:: python

    GRAPHENE = {
        'MIDDLEWARE': (
            'path.to.my.middleware.class',
        ),
    }


``RELAY_CONNECTION_ENFORCE_FIRST_OR_LAST``
------------------------------------------

Enforces relay queries to have the ``first`` or ``last`` argument.

Default: ``False``

.. code:: python

    GRAPHENE = {
        'RELAY_CONNECTION_ENFORCE_FIRST_OR_LAST': False,
    }


``RELAY_CONNECTION_MAX_LIMIT``
------------------------------

The maximum size of objects that can be requested through a relay connection.

Default: ``100``

.. code:: python

    GRAPHENE = {
        'RELAY_CONNECTION_MAX_LIMIT': 100,
    }
