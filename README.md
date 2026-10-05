The data file named companies_and_staggered_returns.xlsx contains the final data. There is one tab for each "stagger" with the original adjusted close prices, log returns, weighted log returns, sector betas, and residual sector betas. 

There are a few things to point out:

-  First is that the energy sector return beta (XLE) is negative for the first stagger and much smaller than expected for the other three staggers. This is unexpected but, as far as I can tell, correct. It was computed the exact same way as the other betas, all of which are much more reasonable. I also plotted SPY return vs sector etf returns as well as SPY return and sector etf return over time. The plots visually verify this calculation. 

- Second is that the sector etf residuals are calulated by subtracting both Beta and Alpha from the return. The other option is to only subtract Beta, but that is a decison we can make as a group.

- Finally, chat gpt or other LLM may point out the fact that the weighted least squares is computed incoreectly. I scaled the X and Y series by time weights calculated in class and then ran a regular regression. Chat says that to perform standard weighted OLS, we should use the weights to squared residuals. I kept it how we discussed in class, but could be worth returning to. 


 All of the data needed for each group is in the companies_and_staggered_returns.xlsx under the respective tabs. You will have to merge with the companies dataset if you want the sector or currency for a specific company. The data is in columns for each stock with the rows being the dates. This is unconventional but made sense to collect in this format. It might be easier to transform it into a standard panel dataset to do more filtering by sector and such. You can do this using the melt() function and chat gpt's help. To extract each dataset within the excel file, use the skiprows parameter when loading the data. I did it in the Verifications notebook for an example.
 
