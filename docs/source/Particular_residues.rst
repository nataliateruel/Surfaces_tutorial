Particular residues
=====

Interaction calculation
------------

To calculate interactions between particular residues of interest and residues of a protein, you use::

      python surface_cont_res.py -f pdb_file.pdb -res res1,res2,res3 -o csv_output.csv -def atomtypes_definition.def -dat atomtypes_interactions.dat
      
that will provide a calculation of the interactions between the residues of interest (written as resName-numRes-chainID) and every other residue in the structure, including intrachain interactions.

Visual output
----------------

To generate a pymol session visually presenting the calculated results, you might use::

      python image_surfaces.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse
      
or utilize extra customizations that are better explained at `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_.

Example application
----------------

For our **particular residues** application we will use the SARS-CoV-2 Spike containing the mutation D614G (`PDB ID 7EAZ <https://www.rcsb.org/structure/7eaz>`_), now known to contribute to evolutionary fitness through different molecular mechanisms. With this function of Surfaces we will be able to quickly evaluate both intra and interchain interactions from the residue in question, GLY614, to assess posible impacts in folding or conformational equilibrium connected to transmissibility.

First we need to clean the structure from any non-defined atom, such as heteroatoms - in the case of this example, NAG and BMA atoms:

      python clean_structure.py -f 7EAZ.pdb -def AMINO_FlexAID.def
      
And you will have created the clean_7EAZ.pdb file.

Now, for the interactions evaluation, you will use::

      python surface_cont_res.py -f clean_7EAZ.pdb -res GLY614A,GLY614B,GLY614C -o 7EAZ_output.csv -def AMINO_FlexAID.def -dat FlexAID.dat

With the residue of interest specified for each chain in which it exists. And now you have created the output file 7EAZ_output.csv with the pairwise interactions of the residues GLY614A, GLY614B and GLY614C and all residues from Spike.

To map this evaluation back to the structure and visually check your results, you can run::

      python image_surfaces.py -f clean_7EAZ.pdb -c 7EAZ_output.csv -o 7EAZ_visual_output.pse -res GLY614A,GLY614B,GLY614C
      
Now you have a representation of your results in the pymol session 7EAZ_visual_output.pse. All the existing interactions are represented and saved as enabled objects due to the specification of the residues of interes using -res - to know more about it, check the `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_ page. The color scale goes from red for unfavorable interactions, to blue for the favorable ones, and is automatically determined based on the largest absolute value - which is also `Customizable <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#visual-outputs>`_.

      
