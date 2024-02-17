
![CoSb3_Co-BS](https://github.com/PetersonChemLab/ProjectedBS_Plotter/assets/160284370/4d185e9b-a465-4ff2-a531-c690f71af1b7)

# ProjectedBS_Plotter
This repository contains a Jupyter notebook and python .py file for plotting "fatband" style band structure plots from VASP calculations using atom-projected eigenvalues. There are 2 kinds of input needed to run this notebook:
1. PBAND_{element}_SOC.dat file(s)
2. KLABELS file

Both of these files are produced Vaspkit (https://vaspkit.com/) using option 213 ("Projected Band Structure of Each Element"). To generate a plot, run this notebook in the same folder where the input files are located. Input variables are:
1. element
    - Name of the element for projection. NOTE: You *must* have a corresponding PBAND_{element}_SOC.dat file.
2. ylim (-1 to 1)
    - Energy range to plot in eV
3. xlim (None)
    - k-point range to plot. Inspect KLABELS file if you want to zoom to a specific section, otherwise full path is plotted
4. band_color ('lightcoral')
    - fill color for the fat bands. suggested colors include 'lightcoral','lightblue','lightgreen','lightgray', and 'plum'
5. fatband_scale (0.1)
    - scalar for the width of the fatbands. Larger -> fatter
6. figsize (12 by 5)
    - figure size (w x h)
7. savefig_filename (None)
    - if defined, will save the output file as an image in the working directory. use '.png' or '.jpg'
    
Library dependencies:
1. numpy (https://numpy.org/)
2. matplotlib (https://matplotlib.org/)
