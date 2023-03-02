Protein-Protein
=====

Interaction calculation
------------

To calculate pairwise interactions between residues of different strutural units, you use::

      *python surface_cont.py -f pdb_file.pdb -c1 ABC -c2 DE -o csv_output.csv -def atomtypes_definition.def -dat atomtypes_interactions.dat*
      
that will provide a calculation of the interactions between residues of the first group of chains (A, B and C in the example) and residues of the second group of chains (D and E in the example).

Visual output
----------------

To generate a pymol session visually presenting the calculated results, you might use::

      python image_surfaces.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse

or utilize extra customizations that are better explained at `here <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_.

Example application
----------------
