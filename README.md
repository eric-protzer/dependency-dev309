# dependency-dev309

You can use this github repistory to create analyses of how much your country's export sector depends on certain public goods. You just need to input your country's ISO code, the ISO codes of its peers, and the years (from 1995 to 2016) you want to look at.

Instructions:

1. Click here:
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/eric-protzer/dependency-dev309/master)
2. WAIT for the server to go live
3. Click on the file "Dependency Graphing 4.0"
4. In cell #1, change the ISO codes to the countries you want to look at. Set the variable 'mycountry' to your own country (replace 'VNM'), and set the variable 'peers' to a list of your country's peers. Then, set the list of years to the years you want to look at (they must be within the range 1995 - 2016).
5. Run the script by going to the tab "Cell" and then clicking "Run All." 
6. Wait again for the script to run.
7. Scroll to the bottom for the graphs. 

Alternatively, you can download "data_out.csv" to do whatever you want with it. This is a panel dataset which reports dependency coefficient and 95% CI for each variable, for each country in each year. 

Slides with an overview of data and methodology: https://drive.google.com/open?id=1_o9yvmCDM-Ky7r-BUT9ZXhg1VPrKoOv43AXx-tRYkl8
