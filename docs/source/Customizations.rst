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
