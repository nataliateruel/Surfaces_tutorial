Preprocessing
=====

Protein structures
------------

In order for Surfaces to evaluate an atom, this particular atom must be specified in the .def file of choice. The default .def file we offer, AMINO_FlexAID.def (from `FlexAID software <https://pubs.acs.org/doi/10.1021/acs.jcim.5b00078>`_), already contains the definition of all residues' atoms. To clean the structure from any non-defined atom, you might use::

   python clean_structure.py -f pdb_file.pdb -def def_file.def
   
You will see examples of usage of this script in `Protein-Protein <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-protein.html#example-application>`_. To customize the atom types definition, you can check `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#atom-type-definitions>`_.

Ligands
----------------

One automated customization that is avaliable is the one to create atom type definitions for ligands of interest. To use it you will need to create and  a pdb file with only the ligand of interest using the following functions::

   python crate_lig_file.py -f pdb_file.pdb -lig LIG
   python ligand_atomtypes.py -fl LIG.pdb
   
After updating the .def file with the ligand of interest, you may clean the complex structure keeping the ligand atoms::

   python clean_structure.py -f pdb_file.pdb -def custom_def_file.def

You will see examples of usage of these scripts in `Protein-Ligand <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-ligand.html#example-application>`_.

Structural models
----------------

Since Surfaces method is based on the area in contact between atoms, it is important to check if the proximity between atoms is realistic when it comes to modeled structures. Atoms that are too close together would create steric clashes and therefore have an extremely unfavorable interaction, but from the area in contact perspective this would not be seen. In order to identify possible steric clashes that would make particular results unreliable, you can test your structure using::

   python steric_clashes.py -f pdb_file.pdb
