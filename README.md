# Digitize Plots

In my personal time, I've been downloading and digitizing plots from different code standards and ASHRAE handbooks in order to make a lightweight calculator to obtain flow rates, transmittance, etc.

## Installation & Usage

After downloading the repository, at the minimum your project should contain: 
* digitizedPlots.xlsm
* main.py

To use the calculator:
1. Open digitizedPlots.xlsm
2. On the CALCULATOR sheet, select a plot type from the dropdown on Row 3.
3. Specify the type of curve under the TYPE dropdown in Columm B.
4. Enter a value in either Column C or Column D.
5. Press CALCULATE to obtain the other point on the curve.

This project also contains a Python script ('main.py') that can extract all images from a PDF. As an example in this project, I extracted all the images inside of the ASHRAE 2011 handbook and stored the output inside of the 'images' directory.

## Digitizing Web Plots
The data in the spreadsheet is obtained from images of different plots that are uploaded to [WebPlotDigitizer ](https://apps.automeris.io/wpd/) with some pre-processing to remove text and crop if necessary. This generated a .csv file that I downloaded and copied into 'digitizedPlots.xlsm'.

## Fitting Curves
I used a combination of fitting to Power curves and using Newton's method to solve for a polynomial fit. However, I believe that Newton's method could have been applied to all data sets.

## License
[MIT](https://choosealicense.com/licenses/mit/)