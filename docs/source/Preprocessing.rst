Preprocessing
=====

Protein structures
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Ligands
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

Structural models
----------------

Since Surfaces method is based on the area in contact between atoms, it is important to check if the proximity between atoms is realistic when it comes to modeled structures. Atoms that are too close together would create steric clashes and therefore have an extremely unfavorable interaction, but from the area in contact perspective this would not be seen. In order to identify possible steric clashes that would make particular results unreliable, you can test your structure using::

   python steric_clashes.py -f pdb_file.pdb
