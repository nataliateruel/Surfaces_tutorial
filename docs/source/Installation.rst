Installation
=====

There are a few dependencies for Surface's python scrips. To install those, simply type::

	pip install pymol
	pip install pandas

inside your terminal.

Another necessary step is to compile Vcontacts. In order to do so, you might use::

   	clang Vcontacts-v1-2.c -o vcon
   
or also::

   	gcc -c Vcontacts-v1-2.c

   	gcc Vcontacts-v1-2.o -o vcon
