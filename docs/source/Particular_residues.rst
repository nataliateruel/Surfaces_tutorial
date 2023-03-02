Particular residues
=====

Interaction calculation
------------

To calculate interactions between particular residues of interest and residues of a protein, you use::

      python surface_cont_res.py -f pdb_file.pdb -res res1,res2,res3 -lig LIG -o csv_output.csv -def atomtypes_definition.def -dat atomtypes_interactions.dat
      
that will provide a calculation of the interactions between the residues of interest (written as resName-numRes-chainID) and every other residue in the structure, including intrachain interactions.

Visual output
----------------

To generate a pymol session visually presenting the calculated results, you might use::

      python image_surfaces.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse
      
or utilize extra customizations that are better explained at `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_.

Example application
----------------
