==========
User Guide
==========

The JEDI Analysis produces output and performs the underlying calculations in redundant internal coordinates, 
whereas the input data is given in cartesian coordinates. The main routine of the JEDI Analysis converts the 
cartesian coordinates and the Hessian into redundant internal coordinates to then apply the
harmonic approximation to calculate the energies in the redundant internal coordinates.
To achieve the switching between the cartesian and redundant internal coordinates, the B-Matrix is calculated according to 
V. Bakken, T. Helgaker, J. Chem. Phys. 117 (20) 2002. 

General structure
-----------------

For the analysis a Jedi object needs to be created which has the necessary functions and can store the important values. 

1.  ``Jedi = Jedi(opt, strain, modes)`` where "opt" and "strain" are Atoms objects and "modes" is a VibrationsData object 

2.  ``Jedi.run()`` or ``Jedi.partial_analysis(indices)`` will do the analysis automatically

3.  Finally VMD readable outputs can be generated with ``Jedi.vmd_gen()`` 
    which defines bonds colors
    according to the strain energy stored in them (green: low strain, yellow: medium
    strain, red: high strain; transitions are fluent).







