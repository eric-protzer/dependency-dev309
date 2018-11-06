# dependency-dev309

You can use this github repistory to create analyses of how much your country depends on certain public goods. You just need to input your country's ISO code, and the ISO codes of its peers.

Instructions:

1. Click here:
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/eric-protzer/dependency-dev309/master)
2. WAIT for the server to go live
3. Click on the file "Dependency Graphing"
4. In cell #2, change the ISO codes to the countries you want to look at. Set the variable 'mycountry' to your own country (replace 'VNM'), and set the variable 'peers' to a list of your country's peers. 
5. Run the script by going to the tab "Cell" and then clicking "Run All." 
6. Wait again for the script to run. Since this is running off a free server, not your local machine, it will run slowly. You can go do something else and check for the results later. 
7. Scroll to the bottom for the graphs. 

## Notes
- If you're tech-savvy and want to run this more quickly, you can download the github contents and run the Python Notebook on your own computer as opposed to via the server. To do this you'll need to install Anaconda.

- In case you're interested in doing this analysis on your own from scratch, this is (at a high level) the methodology I followed:
1) Download HS trade data and extract a list of all HS-coded products. Use the R package "concord" (developed by MIT economists) to get a list of which HS products correspond to which NAICS products. 
2) Download the US BEA's 2007 input-output table (which has the most detailed data available in a reasonably recent year). Convert their concordance page to something more machine-readable (I did this by hand). Use that to get a list of which NAICS products correspond to which BEA products (they use their own classification system). 
3) Using these product concordance tables, employ a statistical programming language (I used Python) to aggregate the HS trade data first to the NAICS and then to the BEA level. As you aggregate, you'll notice that some products correspond to several products at an aggregated level. In principle there are several ways you can handle this; my approach was to spread the products evenly into the higher-level categories. Having aggregated the trade data, filter it to include only the countries and years you're interested in. 
4) Filter the BEA's input-output table for the inputs you want to examine. I looked at electricity, truck transport, rail transport, and wired communications. Use consumption of each input in each BEA sector to develop sector-wise weightings for your regressions. 
5) Conduct the regressions specified in the lecture notes, iterating through inputs and years in different regressions as needed. 
6) Graph results as you desire. 
