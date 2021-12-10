# martini3_namd
NAMD-style parameter file for Martini 3 force field

An example parameter file for running the Martini 3 force field in NAMD. The parameter file currently only includes information for DOPC, DOPE, and W. If other Martini 3 beads are desired, use the appropriate martini_v3\*itp files and add into the martini_3.namd.prm file.

Comments in the martini_3.namd.prm file describe how to change units between the martini_v3\*itp (GROMACS-style) and martini_3.namd.prm (NAMD-style) formats. For example, for bonds, the martini_v3\*itp units are kJ/mol/nm^2 and the martini_3.namd.prm units are kcal/mol/A^2.

The largest difference is bewteen Lennard-Jones (LJ) parameters. GROMACS lists the LJ parameters in "sigma epsilon" format and NAMD uses "E_min R_min" format. As per the first paragraph of the Wikipedia page (https://en.wikipedia.org/wiki/Lennard-Jones_potential), E_min = -epsilon and R_min = 2^(1/6)sigma. The units must be adjusted from kJ and nm to kcal and A.
