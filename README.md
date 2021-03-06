# Election-Analysis

## Overview of Project

Assist Colorado Board of Election employee Tom with an election audit for U.S. Congressional Precinct in Colorado.

### Purpose

Due to multiple methods of voting; in-person, punch cards, and Direct Recording Counting, the task of counting votes and auditing the results of the election and certifying the results can be tedious.  Currently this process is managed manually through Excel. Tom would like to automate the election verification programmatically using Python.  If successful, this automation could be leveraged by other districts and for Senate elections.

## Analysis and Challenges

The challenge is to bring a novice up to speed with Python to take a manual tedious process into a more robust automated process.  This requires a review of the current method and develop an understanding of what inputs are available to generate the required outputs that will be used validate the election results and sent to the interested parties. The rest of this analysis will be addressing the approach taken to achieve Tom's goal of an automated report.

### Analysis of Election Analysis Requirement

Upon Analysis of the election analysis requirements, there are multiple opportunities for improvement that could automate the process of the election analysis and provide powerful data and reporting.  The Election Results report must output the following: 

*  Total Votes
*  County voting results displaying the county, quantity of votes for each county and percentage of votes for each county. 
*  The county with the largest voting turnout.
*  The candidate's names, quantity of votes received and percentage of votes received per candidate.
*  Declaration of the winner which provides winning candidates name, quantity of votes, and winning percentages.
*  Provide a report of above results in a command line format and .txt format.

### Analysis of the Approach to Automate Election Analysis Requirements.

After reviewing the data file, it is determined that through Python the best approach is to use repetition and conditional statements with logical operators and print statements to pull the required information from the file, run calculations, determine winning conditions, and output the results in an attractive and readable format from both the command line and in .txt format.  Both 'for' loops and 'if' statements will be the backbone of the code to achieve these results. 

To run the repetition and conditional statements we will first need to create variables to store relevant information from the csv file and store it for use later.  In this case, the data that we are most interested in storing is information regarding the candidates running for office and data as it relates to county turnout and relevant voting percentages.

*   The screenshot below highlights the variables used to create lists and dictionaries to store the data as it relates to candidates and county specific data.

![ListDictionary](Resources/ListDictionary.png)

*  With variables created we can then open the file and set the initial vote count to zero.  This allows us access to the required data and clear any residual data stored in a variable to ensure we get accurate vote counts for analysis later. From there we can then begin to pull data to be used for calculations later.

*  This code snippet opens the file that will be used to pull required data to run the analysis
 
![ReadCSVfile](Resources/ReadCSVfile.png)

*  While this snippet is the code that sets the vote count to zero.

![SetsVoteCountZero](Resources/SetsVoteCountZero.png)

From here we begin to collect the candidate and county specific data using 'for' loops and conditional statements.  The code containing the 'for' loops and conditional statement goes through each row of the data and stores the relevant information while indexing.  This will allow us to get each candidate and each county and store vote counts for each variable to be used for analysis later in the code.  

* This use of 'for' loops and conditional statements to gather candidate and county information can be seen below.

![For_Loop_If_Cond](Resources/For_Loop_If_Cond.png)

Now that we have the data pulled and stored in variables, now the fun begins.  With the data acquired from the .csv file for the candidate and counties, we can use Python to run mathematical calculations to show how many people voted for a particular candidate, percentage of votes for that candidate, and the amount of votes cast in each county and the precentage of total votes each county and candidate received.

* The code snippets below show the acquisition of vote counts and the application of a mathematical formula that calculates the percentage of votes acquired by candidates and what percentage of votes did each county cast.

![CandidateAnalysis](Resources/CandidateAnalysis.png)  ![PerCountyAnalysis](Resources/PerCountyAnalysis.png)

Now that we have all this data and calculations complete, we need to make it meaningful to the people that will review this data, particularly Tom.  Formatting is an important step to make this data more impactful.  Below you will find the snippets of code that were used to format the output of the data to not only make the information more legible but also presents the data in an attractive manner that makes it easier for the user to read and understand. The following snippets are run in different places of the code to handle the output of the data to be displayed on both the terminal and as a .txt file.

![CodeToFormatTotalVoteForTeminalTextPrint](Resources/CodeToFormatTotalVoteForTeminalTextPrint.png)    ,    ![WinnerTerminalTextOutput](Resources/WinnerTerminalTextOutput.png)

### Summary of Output Terminal Display and .txt File.

 The output on the left is the report displayed on the terminal and on the left is the same data displayed in a .txt format.

![TerminalOutput](Resources/TerminalOutput.PNG) , ![DataSavedToTxtFile](Resources/DataSavedToTxtFile.PNG)


### Results of the Automation of Election Analysis

By reviewing the output screen shots above, we can easily determine the following:

* There were 369,711 total votes casted.  
* Denver had the largest voter turnout with 306,055 votes followed by Jefferson County and Arapahoe, respectively.  
* Diana DeGette won the election capturing 272,892 votes for a winning percentage of 73.8%.
* Charles Casper Stockham and Raymon Anthony Doane finished second and third, respectively.

## Election-Audit Summary

Now that the Colorado Board of Election committee can see the quality of data that this Python based tool out puts and the amount of time that will be inherently saved by taking a process that was manual and now created through automation, I propose that this code is distributed to audit elections, both federal and local throughout the various districts.

The use of this codes to audit elections, both federal and local throughout the districts will:
 
 * Streamline the process as the code will perform all the calculations, reducing the need to have an individual in each district responsible for counting and validating the results
 * Minor code changes can be made to import the data from other districts, reformat it and create reports that are consistent in look and feel from one district to the next.
    * Some of those changes may be variables that can identify if the election is run for local elections or federal elections.
 * Another benefit is with a uniformed method of pulling data, calculating, and reporting results, it makes it easier to identify historical trends.  The code can be set up to segregate data out based on year. If the code is written to account for the year of each election, it would become easier to pull this data in and run calculations that could identify voter trends year over year.  

Being able to utilize the data to its fullest potential would be extremely difficult to accomplish if each district captured and processed results using their own methodologies. Leveraging Python and this code would require fewer people and less time to evaluate the data and would allow for features to be added on that could be quickly utilized by other districts for deeper analysis of data on a larger scale over many years.

