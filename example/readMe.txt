
Files:
======

readMe.txt - this file
ReleaseNotes.txt - input/output file formates
runMe.s    - script for running period finder and DEBiL fitter


bul_sc42_2087.dat - example OGLE light curve
bul_sc46_797.dat  - example OGLE light curve
bul_sc49_538.dat  - example OGLE light curve


periodS2    - Period finder
periodS2.c  - source code

periods.txt - Period finder results output
periods.err - Period finder error log


debil    - DEBiL fitter
debil.c  - source code

list.txt - DEBiL list input
list.dbl - DEBiL results otuput
list.err - DEBiL error log



Running the script:
-------------------
just enter "runMe.s"
will run on all the *.dat light curves files in the directory
besides "runMe.s" and the *.dat files, you don't need anything else



Period finder:
--------------

Compile:  gcc periodS2.c -o periodS2 -Wall -lm -O4 

Run:      periodS2 bul_sc42_2087.dat periods.txt periods.err




DEBiL fitter:
-------------

Compile:  gcc debil.c -o debil -Wall -lm -O4

Run:      debil list.txt list.dbl list.err 
