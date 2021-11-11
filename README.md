# Election-Analysis

## Overview of Project
Assist Colorado Board of Election employee Tom in an election audit for U.S. Congressional Precinct in Colorado.

### Purpose
Due to multiple methods of voting; in-person, punch cards, and Direct Recording Counting, the task of counting votes and auditing the results of the election and certifying the results can be tedious.  Currently this process is managed manually through Excel. Tom would like to automate the election verification programmatically using Python.  If successful, this automation could be leveraged by other districts and for Senate elections.

## Analysis and Challenges
The challenge is to bring a novice up to speed with Python in an effort to take a manual tedious process into a more robust automated process.  This requires a review of the current method and develop an understanding of what inputs are available to generate the required outputs that will be used validate the election results and sent to the interested parties. The rest of this analysis will be addressing the approach taken to achieve Tom's ultimate goal of an automated report.

### Analysis of Election Analysis Requirement

Upon Analysis of the election analysis requirements, there are multiple opportunities for improvement that could automate the process of the election analysis and provide 

*  The code operates in a very serial manner. 
*  Per ticker index, code is run one line at a time.  
*  Data is placed in the appropriate column on the designated output work sheet one ticker at a time.  
    --Starts with ticker 0 and runs through each line of code to calculate the volume, then the starting price, ending price, and then the post calculates the return. Then it moves on and repeats the process for tickers 1 through 11. A very serial process that requires movement across multiple tables and sets of data.

![OriginalCodeLineByLineReduced](resources/OriginalCodeLineByLineReduced.png)


### Analysis of Opportunities of improvement
After evaluating the original code above, better use of arrays within the code could greatly improve the performance of this analysis tool.  By using arrays one can store larger sets of data in relation to other arrays.  With a single loop more data can be collected and stored in a computer's memory to then be pushed to the output file destination at one time.  

*   The screenshot below can be found in both the original and refractored code.  This code allows each stock ticker symbol to be stored to an array and then recalled through indexing.
![DimTickers](resources/DimTickers.PNG)

*****Place other images highlighting use of arrays in refractored code

### Results of Original Code Vs Refactored Code


## Summary

### Advantages and Disadvantages of Refactoring Code

### Advantages and Disadvantages of Projects Original and Refactored code.
Conclusion number one is the month of May appears to be the best month to start a kickstarter campaign and have a successful campaign.  While June and July appear to be the next best option for both starting and having a successful kickstarter.  
The second conclusion is the month of December appears to have the least activity with regards to starting a kickstarter and the lowest success rate.


- What can you conclude about the Outcomes based on Goals?
Based on the Outcomes Based on Goals analysis, one can conclude that there is a a direct connection between the goal amount and whether fund raising campaign is successful or fails.  Goals set too high may not be reached and goals set too low may be insufficient to fund a project.  One must fully understand what is required to fund their projects and must set a number that is appropriate to reach their funding goals. 

- What are some limitations of this dataset?
The dataset as provided in this exercise fails to link the success and failure rates based on the launch month of the kick starter in relation to the goal amount for that kickstarter.  It would be interesting to see if the goals set for the month of May were more in line with a goal level set that have shown higher levels of success as highlighted in the Outcome vs Goals chart. 
Another issue with the dataset provided, is it does not consider any macro or micro economic factors that my impact the success or failure rate of any given kickstarter campaign.  Macro factors such as recessions or micro factors such as less discretionary spending during the holidays than compared to the summer months.

- What are some other possible tables and/or graphs that we could create?
In addition to a table that cross references the range of goals for successful and failed kickstarters in the month of May, a table that shows year over year performances of kickstarters of multiple industries.  This information would prove to be valuable as it could show if certain industries are falling out of favor.  Are kickstarters associated with publishing falling out of favor when compared to technology kickstarters?  How do food kickstarter campaigns success/fail rates over multiple years trend in comparison to theater kickstarters.  This would be helpful to see this historical analysis so if Louise were to decide to have another fundraising campaign in the future, she would be more confident in its likelihood for success.
Another interesting view would be how quickly did the successful kickstart campaign reached their goals.  How many days did it take for successful campaigns to reach their goals in relation to their start dates?  This could be helpful for Louise to set not only a reasonable goal, at the correct time of year, but also to provide it enough time.
