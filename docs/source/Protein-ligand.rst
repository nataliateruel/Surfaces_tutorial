Protein-Ligand
=====

Interaction calculation
------------

To calculate interactions between a ligand and residues of a protein, you use::

      python surface_cont_lig.py -f pdb_file.pdb -c ABC -lig LIG -o csv_output.csv -def atomtypes_definition.def -dat atomtypes_interactions.dat
      
that will provide a calculation of the interactions between residues of the group of chains (A, B and C in the example) and atoms of the ligand (LIG in the example).

Visual output
----------------

To generate a pymol session visually presenting the calculated results, you might use::

      python image_surfaces_lig.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse
      
or utilize extra customizations that are better explained at `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_.

Example application
----------------

SARS-CoV-2 PLpro PROFLAVIN (PRL) (`PDB ID 7NT4 <https://www.rcsb.org/structure/7NT4>`_)
