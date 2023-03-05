How to uninstall
=====

The first step in using **Surfaces** is to install Python. Details for installing Python can be found on the `Python downloads page <https://www.python.org/downloads/>`_.

Another essential step is to install Pymol by following the instructions on the Pymol Wiki for your operating system - `Mac <https://pymolwiki.org/index.php/MAC_Install>`_, `Linux <https://pymolwiki.org/index.php/Linux_Install>`_ or `Windows <https://pymolwiki.org/index.php/Windows_Install>`_.

To access all **Surfaces** codes, you can clone the repository::

	git clone https://github.com/nataliateruel/Surfaces

There are a few dependencies for **Surfaces**' Python scripts. You can install them by running the following command inside the **Surfaces** directory::

	cd Surfaces
	pip install -r dependencies.txt

.. note::
	
	It is important to install the dependencies for the same version of Python that you plan to use for running the scripts.

Another necessary step is to compile Vcontacts. For Mac and Linux machines, you can use::
	
   	clang Vcontacts-v1-2.c -o vcon
   
or also::

	gcc -c Vcontacts-v1-2.c
	gcc Vcontacts-v1-2.o -o vcon -lm

For Windows, make sure to have a functional C compiler installed, such as the one presented `here <https://www.wikihow.com/Run-C-Program-in-Command-Prompt>`_.

.. note::
	
	For the subsequent usage steps, we recommend running your structure analyses within the **Surfaces** directory.
