# HST_MagellanicCorona
Observational Evidence for a Massive Magellanic Corona (Krishnarao et al. 2022)

This repository contains data and python notebooks associated with Krishnarao et al. (2022): Observational Evidence for a Massive Magellanic Corona

## Key Data Tables
Data/FIT_AND_CLOUDY_RESULTS.fits
    Table that contains all voigtfit and cloudy model results for fit absorption line components flagged as possibly part of the Magellanic System
    
Data/SUMMED_ION_COLUMNS_wHII.fits
    Summed ion column densities of all ions for each source. 
    For low ions, this is all components with v>150 km/s
    For C IV and Si IV, this is all components with v>150 km/s and >1dex excess of observed column than Cloudy model predictions
    For OVI, this is all components with v>150 km/s
    Column density errors of -1 imply upper limits

python notebooks titled by the figure number in the paper are used to recreate the paper figures. 




The SummaryResults folder contains images and a summary text file of all the results of our Voigt profile fitting of 28 HST/COS sightlines. 

There is a folder for each source analyzed:
In each folder there is a txt file that contains detailed notes and all fit parameters for ions. 
These notes are grouped in the same way that fitting was done, first all low and intermediate ions, then CIV and SiIV, and lastly OVI when it is available. 

When it seems reasonable, we have performed voigt fits on OVI, but at times we do not see a reasonable way to get a good continuum fit or identify components. In these cases, the OVI is not fit, but still displayed in the plots described below. 

The bottom of this file also has the “flagging” that we have done for each of the fit components. The last item for each row of these flags marks “c#” to match components later on easily. The ordering of these flags match the same ordering that the fit results are printed out in (and how the component results are saved). 
Here is a key of what these flag values are:

                          "MW":"Milky Way”, 
                          "IVC":"Intermediate Velocity Cloud",
                          "HVC":"High Velocity Cloud",
                          "MSys":"Magellanic System”, - typically I mark anything Magellanic with just this tag
                          "MStr":"Magellanic Stream",
                          "MB":"Magellanic Bridge",
                          "MC":"Magellanic Corona",
                          "U":”Unknown / Uncertain”, -  I almost mark everything with this, it doesn’t mean too much so ignore mostly
                          "BB":"Bad Linewidth (b)",
                          "S”: "Saturated - Lower Limit",
                          "C": "Contaminated - Use With Caution",
                          "B": "Bad Fit - Do Not Use”,
                          “LL”:"Lower Limit”,
                          “UL”:”Upper Limit”,

There are 4 total files of plots, two are .png and two are .svg 
The figures are all of the normalized spectra and their fit results. The files ending in _zoom are zoomed in to the velocity range covering just where there is absorption being fit. 
The data are plotted in red-orange, which some red shading encompassing the errors of the data. 
The continuum and continuum fit error are marked with black horizontal lines (dashed and dotted)
The full fit profile in plotted as a black line
Individual components for the ion labeled in the upper left of the panel are plotted in teal. 
The spectra are ordered following the same ordering you have used in your ISM-meas plots. 
