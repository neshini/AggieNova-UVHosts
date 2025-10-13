# AggieNova-UVHosts
All the work I did for Dr. Peter Brown over the course of 2024-2025.

## Kcorrections
Kcorrections.ipynb - Reads in the photometry for a galaxy from 'FinalPhotUV.dat', pulls that galaxy's spectrum from Blast, computes the k values, subtracts k from observed photometry, and saves the final kcorrected values in 'KcorrectedFinalPhotUV.csv'

## Photometry
UVOT_SNvsGal.ipynb - Reads in 'FinalPhotUV.dat', 'KcorrectedFinalPhotUV.csv', 'outputmags_color.dat'. Makes different color comparison plots like UVW1-V(Host) vs B-V(Host) of original values, then k-corrected values for the same colors. Very messy, x and y values for the reddest and bluest galaxies found manually.
"3a.png" - uncorrected UVW1-V(Host) vs B-V(Host)
"K_3a.png" - Kcorrrected UVW1-V(Host) vs B-V(Host)
"3b.png" - uncorrected UVW1-UVW2(Host) vs B-V(Host)
"K_SN_3b.png" - Kcorrrected UVW1-UVW2 vs B-V, plots host as green o, sn as purple x.
"K_SN_ColorvMag.png" - Kcorrrected Color(UVW2-V) vs Mag(V), plots host as green o, sn as purple x.
"plots" folder - has every combination of filter vs filter (ex: B vs V)

## Blast
Blast_SNwork.ipynb - Begins with experimenting with Blast. Reads in 'FinalPhotUV.dat', checks if Blast has data for each SN, if missing, saved in 'missingSN', if exists, grabs data of SN for properties specified, saved into dictionary. Creates property vs property plots, and property vs color plots (the kcorrected colors from before).
"prop_plots" folder - has every combination of property vs property (ex: log mass vs log ssfr)
"prop_col_plots" folder - has 2 plots per image, left is host color vs property, right is sn color vs property

## Galaxy colors
making_3color_images.ipynb - A generalized code, given an SN name, and obsID from MAST archive, makes a 3 color images with blue = UVM2, green = U, red =  V. Details given in file. This is the code I used to create images for the reddest and bluest galaxies,2011B and  2011aa respectively.

## Poster
Presentation.ipynb - takes all the plots in the folder 'prop_col_plots' and lines them up to create one image, "slide_background.png".
