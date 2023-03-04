Preprocessing
=====

Protein structures
------------

In order for **Surfaces** to evaluate an atom, it must be specified in the .def file. The default .def file provided by **Surfaces**, AMINO_FlexAID.def (from `FlexAID software <https://pubs.acs.org/doi/10.1021/acs.jcim.5b00078>`_), already contains the definition of all the atoms of the 20 amino acids. To remove any non-defined atoms from the structure, you can use::

   python clean_structure.py -f pdb_file.pdb -def def_file.def
   
You can find usage examples of this script in the `Protein-Protein <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-protein.html#example-application>`_ section. To customize the atom type definitions, you can read the `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#atom-type-definitions>`_ section.

Ligands
----------------

One automated customization avaliable is the one to create atom type definitions for ligands of interest. For this, you will need to create and assess a .pdb file with only the ligand of interest using the following functions::

   python crate_lig_file.py -f pdb_file.pdb -lig LIG
   python ligand_atomtypes.py -fl LIG.pdb -def def_file.def
   
After updating the .def file with the ligand of interest, you can clean the complex structure while keeping the ligand atoms::

   python clean_structure.py -f pdb_file.pdb -def custom_def_file.def

You can find usage examples of these scripts in the `Protein-Ligand <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-ligand.html#example-application>`_ section.

Modeled structures
----------------

Since the **Surfaces** method is based on the area in contact between atoms, it is important to check if the proximity between atoms is realistic, especially for modeled structures. Atoms that are too close together can create steric clashes, leading to extremely unfavorable interactions. However, from the area in contact perspective, this would not be detected. To identify possible steric clashes that would make the results unreliable, you can test your structure using::

   python steric_clashes.py -f pdb_file.pdb
