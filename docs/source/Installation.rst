Installation
=====

The initial step for using Surfaces is to install python. The details of this installation can be found at the `Python downloads page <https://www.python.org/downloads/>`_.

There are a few dependencies for Surface's python scrips. You can install those inside your terminal::

	pip install pymol
	pip install pandas

To access all Surfaces codes, you can clone the repository::

	git clone https://github.com/nataliateruel/Surfaces

Another necessary step is to compile Vcontacts. In order to do so, you might use::
	
	cd Surfaces
   	clang Vcontacts-v1-2.c -o vcon
   
or also::

   	cd Surfaces
	gcc -c Vcontacts-v1-2.c
	gcc Vcontacts-v1-2.o -o vcon

.. note::
	
	For the following usage steps, we advise running your structure analyses inside the Surfaces directory.
