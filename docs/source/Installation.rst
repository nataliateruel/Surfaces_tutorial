Installation
=====

The initial step for using Surfaces is to install python. The details of this installation can be found at the `Python downloads page <https://www.python.org/downloads/>`_.

Another fundamental step is to install pymol, following the instructions at the Pymol Wiki for each operational system - `Mac <https://pymolwiki.org/index.php/MAC_Install>`_, `Linux <https://pymolwiki.org/index.php/Linux_Install>`_ or `Windows <https://pymolwiki.org/index.php/Windows_Install>`_.

To access all Surfaces codes, you can clone the repository::

	git clone https://github.com/nataliateruel/Surfaces

There are a few dependencies for Surface's python scrips. You can install those inside your terminal using::

	cd Surfaces
	pip install -r dependencies.txt

.. note::
	
	Make sure to install the dependencies to the same version of Python you intend to use when running the scripts.

Another necessary step is to compile Vcontacts. In order to do so, you might use::
	
   	clang Vcontacts-v1-2.c -o vcon
   
or also::

	gcc -c Vcontacts-v1-2.c
	gcc Vcontacts-v1-2.o -o vcon

.. note::
	
	For the following usage steps, we advise running your structure analyses inside the Surfaces directory.
