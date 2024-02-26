This program replicates the OLS and 2SLS instrumental variable regression conducted in the article "The Long Term Effects of Africa's Slave Trade".
Additionally, the graphs within the article are recreated.

Chat GPT prompt used: 
"Could you create a Python program capable of replicating the statistical analysis 
performed in a study where all the relevant data is contained within a file called 
replicationData.csv? The study involves a two-stage regression analysis:

First Regression: Ordinary Least Squares (OLS) Regression
Dependent variable: ln_maddison_pcgdp2000 (log of GDP per capita in 2000).
Independent variables: ln_export_area, longitude, rain_min, humid_max, low_temp, 
ln_coastline_area, island_dum, islam, legor_fr, region_n, ln_avg_gold_pop, 
ln_avg_oil_pop, ln_avg_all_diamonds_pop, colony0, colony1, colony2, colony3, 
colony4, colony5, colony6, and colony7 (the colony variables are called the 
colonizer fixed effect and should be omitted from the regression summary table 
but included in the overall regression estimation).

Second Regression: Two stage Instrumental Variable regression
First Stage
Dependent variable: ln_export_area
Independent instrument variables: atlantic_distance_minimum, indian_distance_minimum, 
saharan_distance_minimum, red_sea_distance_minimum.

Second Stage
Dependent variable: ln_maddison_pcgdp2000
Independent variable: Predicted values of ln_export_area from the first stage of the IV regression.

Please include comments to explain each step and make sure the code is structured 
in a way that is easy to follow. Add functionality to plot the relationship between 
ln_export_area (x-axis) and ln_maddison_pcgdp2000 (y-axis), displaying a scatter plot 
with a trendline. Add functionality to plot the relationship between ln_pop_dens_1400 
(x-axis) and ln_export_area(y-axis), displaying a scatter plot with a trendline. 
Add functionality to plot the relationship between ln_export_area (x-axis) and 
ethnic_fractionalization(y-axis), displaying a scatter plot with a trendline. 
Additionally save all regression summaries printed to two .txt files (one for the 
OLS regression and one for the IV regression first and second stage) and save the 
scatterplot outputs to .jpg files. Additionally, include in all regression summary 
outputs a summary statistics table for the independent variables used excluding the 
colony variables. All files should be saved to the current directory. Please make 
the program organized by functions."
