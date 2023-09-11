=======
Hessian
=======

The Hessian can be calculated via a standard frequency calculation. 
There are two ways to generate the VibrationsData object 

1. Created by ASE through a calculation initiated in the ASE environment
2. Be read from the calculation's output

The script is to be executed with the following command line input:

.. code-block:: console

    python hess_gen.py <input_file.out> <program>

* <input_file.out> : name of the file containing the geometry 
* <program> : program that generated the output (either Q_Chem or ORCA)
