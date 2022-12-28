# ERCOT-Historical-RTM-Price-Data-Process

This code process downloaded ERCOT historical real-time market load zone price data ZIP files into pickle and CSV files

## ERCOT historical RTM Load Zone and Hub Prices can be found here: https://www.ercot.com/mp/data-products/data-product-details?id=NP6-785-ER

### How the code works:
1. Download all zip files into a folder called "zips" then run the code, it will first create a new folder named "unzipped" that contains unzipped Excel files.
2. Then code will then go through each sheet within the Excel file and create one single dataframe that contains the price data from eight load zones and one columns named 'time'. This create a dictionary with the keys being each year and the item contains the dataframe. 
3. Next, the code will read in the pickle file and save each individual year as CSV files.

#### Warning
This code takes a while to run because reading Excel file and iterating through tabs takes a long time.

TODO:
- [ ] Make it into a function that lets user select the years
- [ ] Make save pickle and csv file optional
