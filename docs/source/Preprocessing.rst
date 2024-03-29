Preprocessing
=====
Structure files
------------

If your input structure file is in the format mmCIF instead of PDB, you can easily convert it using::

   python cif2pdb.py cif_file.cif

Protein structures
------------

In order for **Surfaces** to evaluate an atom, it must be specified in the .def file. The default .def file provided by **Surfaces**, AMINO_FlexAID.def (from `FlexAID software <https://pubs.acs.org/doi/10.1021/acs.jcim.5b00078>`_), already contains the definition of all the atoms of the 20 amino acids. To remove any non-defined atoms from the structure, you can use::

   python clean_structure.py -f pdb_file.pdb -def def_file.def
   
You can find usage examples of this script in the `Protein-Protein <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-protein.html#example-application>`_ section. To customize the atom type definitions, you can read the `Customizations <https://surfaces-tutorial.readthedocs.io/en/latest/Customizations.html#atom-type-definitions>`_ section.

Ligands
----------------

One automated customization avaliable is the one to create atom type definitions for ligands of interest. For this, you will need to create and assess a .pdb file for each ligand of interest using the following functions::

   python create_lig_file.py -f pdb_file.pdb -lig LIG
   python ligand_atomtypes.py -pdb LIG.pdb -def def_file.def

Or, in case you do not want the code to rely on importing the pymol library, you can use the .mol2 format as input::

   python ligand_atomtypes.py -mol2 LIG.mol2 -def def_file.def

To evaluate interactions with more than one ligand, you might use as input a list of ligands::

   python create_lig_file.py -f pdb_file.pdb -lig LIG1,LIG2,LIG3
   python ligand_atomtypes.py -pdb LIG1.pdb,LIG2.pdb,LIG2.pdb -def def_file.def

You may also choose a prefix for the custom .def file you are creating by using the prefix input::

   python ligand_atomtypes.py -pdb LIG.pdb -def def_file.def -prefix LIG

Which would create the LIG_def_file.def file with the updated atom type definitions. Otherwise, the default name will be custom_def_file.def.

After updating the .def file with the ligand of interest, you can clean the complex structure while keeping the ligand atoms::

   python clean_structure.py -f pdb_file.pdb -def custom_def_file.def

You can find usage examples of these scripts in the `Protein-Ligand <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-ligand.html#example-application>`_ section.

Modeled structures
----------------

Since the **Surfaces** method is based on the area in contact between atoms, it is important to check if the proximity between atoms is realistic, especially for modeled structures. Atoms that are too close together can create steric clashes, leading to extremely unfavorable interactions. However, from the area in contact perspective, this would not be detected. To identify possible steric clashes that would make the results unreliable, you can test your structure using::

   python steric_clashes.py -f pdb_file.pdb

In case your structure contains steric clashes, you will get warnings as output.
