# CoMo-code-compliance

We obtained a dataset containing code compliance complaints for Columbia, Missouri for the last few years. The dataset required significan cleaning, and the address of each complaint needed to be geocoded into longitude/latitude points before I could start spacial analysis. Most of this can be found in the file, CoMo_CodeCompliance.Rmd.

After the initial round of cleaning and geocoding, additional integrity checks showed many addresses had spelling errors or other mistakes, and hadn't been geocoded -- so I did some additional cleaning. I also briefly took the dataset out of R Studio and used OpenRefine to cluster and combine some categories of code complaints. The original dataset had more than 50 categories -- many of them redundant or similar -- and using OpenRefine, I got the number down to 24. 

I then imported the most up-to-date spreadsheet into R (included in this repository as como-code-violations-orupdated.csv) and used the sf, ggplot, and leaflet packages to make a variety of graphs and maps visualizing the data. I used tidycensus to join the code compliance data to U.S. Census data tracking the population and median household income per block group. This way, I was able to show which block groups had the most code compliance complaints per 100 residents -- and I was also able to graph how lower-income block groups have the highest rates of complaints. All of this can be found in CodeComplaint_analysis.Rmd.

This dataset is being used to identify neighborhoods in Columbia for a broader project about wealth gaps and the way certain areas are kept in poverty.
