# charmm2pdynamo

CHARMM36 and CGenFF parameter files reformatted so the EasyHybrid3 / pDynamo3 parser doesn't fail loading them, 
plus MHET dihedral parameters, which can serve as a template for ligand parameter file.

## Files
- par_all36_prot_pd.prm: CHARMM36 protein parameters
- par_all36_cgenff_pd.prm: CGenFF
- par_water_ions_pd.str: water and ions, reduced to parameter sections
- par_mhe_pd.prm: MHET dihedrals

Modifications: removed title/reference blocks, ATOMS/MASS sections, and CHARMM scripting lines for the parser

**Additional note**
In some cases, when loading a .psf file into EasyHybrid, might be of interest to delete the AUTOG flag at the top and the AUTOGEN section at the end of the file. 

`.crd` files should be converted to `.xyz` via VMD (for example) to avoid some weird conflict with AMBER parser?
