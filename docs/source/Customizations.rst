Customizations
=====

Atom type definitions
------------

The default definition of atom types provided for the 20 amino acids is derived from 40 atom types outlined in the `FlexAID software <https://pubs.acs.org/doi/10.1021/acs.jcim.5b00078>`_::

   ALA | N:11, CA:3, C:2, O:13, CB:3, OXT:13,
   ARG | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:3, NE:12, CZ:5, NH:12, NH1:12, NH2:12, OXT:13,
   ASN | N:11, CA:3, C:2, O:13, CB:3, CG:2, OD:13, OD1:13, ND:11, ND2:11, OXT:13,
   ASP | N:11, CA:3, C:2, O:13, CB:3, CG:2, OD:15, OD1:15, OD2:15, OXT:13,
   CYS | N:11, CA:3, C:2, O:13, CB:3, SG:18, OXT:13,
   GLN | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:2, OE:13, OE1:13, NE:11, NE2:11, OXT:13,
   GLU | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:2, OE:15, OE1:15, OE2:15, OXT:13,
   GLY | N:11, CA:3, C:2, O:13, OXT:13,
   HIS | N:11, CA:3, C:2, O:13, CB:7, CG:4, ND:10, ND1:10, ND2:10, CD:4, CD1:4, CD2:4, CE:4, CE1:4, CE2:4, NE:10, NE1:10, NE2:10,      OXT:13,
   ILE | N:11, CA:3, C:2, O:13, CB:3, CG:3, CG1:3, CG2:3, CD:3, CD1:3, OXT:13,
   LEU | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:3, CD1:3, CD2:3, OXT:13,
   LYS | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:3, CE:3, NZ:9, OXT:13,
   MET | N:11, CA:3, C:2, O:13, CB:3, CG:3, SD:18, CE:3, OXT:13,
   PHE | N:11, CA:3, C:2, O:13, CB:3, CG:4, CD:4, CD1:4, CD2:4, CE:4, CE1:4, CE2:4, CZ:4, OXT:13,
   PRO | N:11, CA:3, C:2, O:13, CB:3, CG:3, CD:3, OXT:13,
   SER | N:11, CA:3, C:2, O:13, CB:3, OG:14, OXT:13,
   THR | N:11, CA:3, C:2, O:13, CB:3, OG:14, OG1:14, CG:3, CG1:3, CG2:3, OXT:13,
   TRP | N:11, CA:3, C:2, O:13, CB:3, CG:4, CD:4, CD1:4, CD2:4, NE:10, NE1:10, CE:4, CE1:4, CE2:4, CE3:4, CZ:4, CZ1:4, CZ2:4,          CZ3:4, CH:4, CH2:4, OXT:13,
   TYR | N:11, CA:3, C:2, O:13, CB:3, CG:4, CD:4, CD1:4, CD2:4, CE:4, CE1:4, CE2:4, CZ:4, OH:14, OXT:13,
   VAL | N:11, CA:3, C:2, O:13, CB:3, CG:3, CG1:3, CG2:3, OXT:13,

Additional atom type definitions for ligands (as detailed in `Preprocessing <https://surfaces-tutorial.readthedocs.io/en/latest/Preprocessing.html#ligands>`_ and `Protein-Ligand <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-ligand.html#example-application>`_) or modified residues can be appended as extra lines using the same formatting pattern.

For **Surfaces**, any other method of defining atoms can be utilized provided that it adheres to the same formatting requirements.

Pairwise interaction
------------

The default pairwise interaction energy matrix provided for the 40 atom types was constructed in accordance with the methodology outlined in the `FlexAID software <https://pubs.acs.org/doi/10.1021/acs.jcim.5b00078>`_::

      1- 1 =        0
      1- 2 =   -119.4
      1- 3 =   -162.9
      1- 4 =   -179.1
      1- 5 =        0
      1- 6 =        0
      1- 7 =        0
      1- 8 =        0
      1- 9 =        0
      1-10 =    157.1
      1-11 =    60.54
      1-12 =   -78.63
      1-13 =   -198.3
      1-14 =   -180.8
      1-15 =    93.26
      1-16 =        0
      1-17 =        0
      1-18 =        0
      1-19 =        0
      1-20 =        0
      1-21 =        0
      1-22 =        0
      1-23 =        0
      1-24 =        0
      1-25 =        0
      1-26 =        0
      1-27 =        0
      1-28 =        0
      1-29 =        0
      1-30 =        0
      1-31 =        0
      1-32 =        0
      1-33 =        0
      1-34 =        0
      1-35 =        0
      1-36 =        0
      1-37 =        0
      1-38 =        0
      1-39 =        0
      1-40 =    159.1
      2- 2 =   -198.9
      2- 3 =   -69.11
      2- 4 =   -149.4
      2- 5 =    194.1
      2- 6 =    165.4
      2- 7 =   -88.78
      2- 8 =        0
      2- 9 =    36.97
      2-10 =    15.81
      2-11 =   -21.59
      2-12 =   -61.99
      2-13 =   -10.06
      2-14 =    61.29
      2-15 =    14.76
      2-16 =        0
      2-17 =     -115
      2-18 =   -123.1
      2-19 =    81.35
      2-20 =        0
      2-21 =        0
      2-22 =    76.92
      2-23 =   -186.1
      2-24 =   -193.7
      2-25 =        0
      2-26 =    13.04
      2-27 =        0
      2-28 =    152.5
      2-29 =        0
      2-30 =        0
      2-31 =    119.8
      2-32 =        0
      2-33 =    121.2
      2-34 =        0
      2-35 =   -40.54
      2-36 =        0
      2-37 =        0
      2-38 =        0
      2-39 =        0
      2-40 =    61.75
      [...]

For **Surfaces**, alternative matrices, whether derived from the same definition of 40 atom types or not, can be employed, provided they are written using the same formatting conventions.

Visual outputs
------------

We have two visual output functions, one of which displays interactions between residues::

      python image_surfaces.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse -cs [bottom_coloe,mid_color,top_color] -cs_range [min_value,max_value] -res res1,res2,res3
   
and the second displays interactions of residues with atoms::

      python image_surfaces_lig.py -f pdb_file.pdb -c csv_output.csv -o pymol_session_output.pse -cs [bottom_color,mid_color,top_color] -cs_range [min_value,max_value] -res res1,res2,res3

The visual outputs funtions, as you can see, have optional customizations, regarding `color scale <https://surfaces-tutorial.readthedocs.io/en/latest/Protein-ligand.html#example-application>`_ (``-cs`` and ``-cs_range``) and `residues of interest <https://surfaces-tutorial.readthedocs.io/en/latest/Particular_residues.html#example-application>`_ (``-res``).

For both **image_surfaces.py** and **image_surfaces_lig.py** functions, the color scale is automatically determined based on the single largest absolute value present in the .csv file. For instance, if the largest absolute interaction value in the .csv file is 5000, the color scale will be defined as [-5000, 5000]. However, to enhance the visual sensitivity of interactions that are less numerically significant or to enable comparison of two results with the same color scale, the user can customize this range by providing an extra input ``-cs_range``. The default colors used are blue for negative values, white for values close to zero, and red for positive values. This, however, can be customized by providing a 3 colors list as an extra input ``-cs``; as an example, to reach the default color scale, the input would be ``-cs [blue,white,red]``. Colors must be named as defined `here <https://www.w3.org/TR/css-color-3/#svg-color>`_.

By default, **image_surfaces.py** will only display the 10% most numerically relevant interactions as enabled objects. All other interactions will be shown as objects and can be enabled by the user through the pymol interface. However, if the user desires to view interactions involving specific residues of interest, such as mutated residues or residues that comprise a particular functional site, the function allows for optional input of these residues by using ``-res`` and will display all their interactions as enabled objects.

In contrast, **image_surfaces_lig.py** will display all interactions as enabled objects by default, represented as separate objects which can be disabled by the user at the pymol interface. However, if the user is interested in a few particular residues, these can be specified as optional inputs ``-res``.

Scaling factor
------------

The values produced by Surfaces considering the atomic areas in contact and the pseudo-energy matrix are not bound to any particular unit. Considering that binding energies are often calculated as kcal/mol and taking 23 experimental points used in the compared results showed in the article (from `Sergeeva et al., 2022 <https://www.biorxiv.org/content/10.1101/2022.08.01.502301v2>`_), we reached a scaling factor currently set as 7.21x10^-4 and used in **surface_cont.py**, **surface_cont_lig.py** and **surface_cont_res.py**.

