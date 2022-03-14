# VBA of Wall Street

## Overview of Project

Client previously asked for code that analyzes the provided green energy stocks for total volume of trades and the % return or loss for one of the two years provided. Client is now asking for the code to be refactors so that it can be run in a shorter time frame.

## Results

The original code used nested for loops. This essentially causes it to run through the entire data set twelve times, once for each ticker. So for the first ticker AY, it collects all of the data it needs in the first 1/12th of the data set and does nothing as it runs through each line of the other ticker entries. At the end of each run it prints out the results for that ticker and then write over those variables in the next run for the next ticker. 

![VBA_Challenge_code_original.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_code_original.png)  

The refactored codes utilizes arrays and an index variable in order to collect all of the information at once. As the for loop reaches the last entry of the first ticker AY, it sees that the next row has a different value in the ticker column and increases our index. The run will then start recording data for the next ticker automatically. This means the algorithm will run through the data set once instead of twelve times. This should theoretically make the code approximately 12 times faster.

![VBA_Challenge_code_Refactored.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_code_Refactored.png)  

Below are screen captures of the change in time for both the 2017 and 2018 data sets provided. This shows that the code is approximately 10 times faster.

![VBA_Challenge_prior_2017.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_prior_2017.png)  ----> ![VBA_Challenge_2017.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png)  
![VBA_Challenge_prior_2018.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_prior_2018.png)  ----> ![VBA_Challenge_2018.png](https://github.com/justinkirk8/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png)  

## Summary

- What are the advantages or disadvantages of refactoring code?

It is difficult to think of advantages or disadvantages with refactoring code. It depends on if the time commitment to refactor the code is worth the time it will save you. If the code is being used on large data sets and is being used frequently then refactoring can be extremely advantageous cause it will save significant time in the long run. If the code is used rarely or used for smaller data sets then the time investment to refactor may not be worth it.
- How do these pros and cons apply to refactoring the original VBA script?

For the data set provided. Refactoring wasn’t necessarily worth it due to it only taking approximately six to seven seconds to run the original code. However, if this code was adapted to be used with a larger group of stocks, then the original code may end up taking a noticeable amount of time which would make refactoring more useful. All that being said, the refactored code is much cleaner.
