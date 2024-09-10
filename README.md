# admp2xyz-release

admp2xyz - a program to convert ADMP log files of G09/G16 to xyz files which can be viewed by moltran (moltran <filename> /nxyz0@geostep /all /nosym /c5000 )

Run command (under Windows):  
admp2xyz.exe


Input files:
admp2xyz.inp          - main input file

See readme.txt for the possible commands in the input file


Commands in the input files:
ADMP <admp_log_file>			! ADMP dump file name (log file of G09/G16)
OUT  <results_file_name>		! Results files names
iBeg <integer>				! Starting step of ADMP trajectory to be processed  [0]
iEnd <integer>				! Final  step of ADMP trajectory to be processed    [1000000]
Each <integer>				! Only Each <n> steps will be processed.            [1]
Bond <Na> <Nb> <Rab>                    ! Atoms with atomic numbers Na and Nb will be considered bounded if distance between them < Rab
Nacf <integer>				! Number of points of velocity autocorrelation function to be calculated (for vibration analysis) [1000] 
MaxS <integer>				! Maximum number of geometries in a single XYZ file [1000000]


Output files:
<results_file_name>.xyz   		! NXYZ file for vizualization with MOLTRAN or other programs
<results_file_name>.dat			! Energies, structure connectivity, instant temperatures etc. for all the processed trajectory points 
<results_file_name>.vib			! Vibrational spectrum calculated on the basis of Fourrier-trensformed velocity autocorrelation function


