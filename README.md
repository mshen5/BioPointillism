# BioPointillism
Code for Yeast Art

For collaboration opportunities, please email YeastArt@gmail.com

To convert a RGB image into a picklist .csv file for the Echo 550 liquid handler, run EchoH.m

You will be prompted for an image name, starting well, and transfer volume

The starting well should be the row/column (ie A1) location of your first color

We recommend 2.5 nL as an initial transfer volume, using yeast between an OD of 1.0 and 1.2

The number of colors used and their order need to be defined in ImgHSV.m using their RGB values

EchoH takes your input image, converts it to HSV colorspace, and calls ImgHSV, which uses a weighted least-squares comparison algorithm to compare your input image to your yeast colors to find the closest color approximation

ImgHSV will additionally output a test display image in yeast colors

EchoH will return echoProgram

Open echoProgram in Excel as a comma-delimited file, and add the following column headings:

Source Row | Source Column | Destination Row | Destination Column | Transfer Volume

Save this file as a .csv file, which is ready to load into Echo Plate Reformat
