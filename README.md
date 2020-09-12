# Election_Analysis
Module 3 repository for Python
*NOTE: Duplicate PyPoll file due to practicing creation & commit to GitHub via VScode and GoogleColab*

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1.  Calculate the total number of votes cast.
2.  Get a complete list of candidates who received votes.
3.  Calculate the total number of votes each candidate received.
4.  Calculate the percentage of votes each candidate won.
5.  Determine the winner of the elction based on popular vote.

## Resources
- Data Source:  [election_results.csv](election_results.csv)
- Software:  
  Python 3.8.3 
  Visual Studio Code 1.47.3 (user setup)
  OS: Windows_NT x64 10.0.19041
  https://colab.research.google.com/notebooks/intro.ipynb
  
## Summary 
The [analysis of the election](Election_Results.png) show that:
- There were 369,711 votes cast in the election.
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were
  - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
  - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
  - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.
   
## Challenge Overview
The Colorado Elections Commission has requested an audit of county voter turnout.  This includes:
  1. The voter turnout for each county
  2. The percentage of votes from each county out of the total county
  3. The county with the higest turnout.

## Challenge Summary
The [analysis of the election](Election_Results.png) shows that:
- There were 369,711 votes cast in the election.
- The counties were:
  - Jefferson
  - Denver
  - Arapahoe
- The county turnout was
  - Jefferson produced 10.5% of the turnout and 38,855 votes.
  - Denver produced 82.8% of the turnout and 306,055 votes.
  - Arapahoe produced 6.7% of the turnout and 24,801 votes.
- The largest county voter turnout was:
  - Denver, which produced 82.8% of the vote and 306,055 votes.
  
As a practice exercise, this analysis was executed in both [VScode](https://code.visualstudio.com/) and [Google Colab](https://colab.research.google.com/notebooks/intro.ipynb).
[PyPoll_Challenge script used for entire analysis](PyPoll_Challenge.py).
Equivalent logic was used for both candidate & county summaries.  Key portion for determining winning candidate and largest county turnout was:

```python
if (votes > largest_county_turnout) and (vote_percentage > largest_county_percentage):
    largest_county_turnout = votes
    largest_county = county_name
    largest_county_percentage = vote_percentage
```

## Future Consideration
This python script could be adapted for any election outcome.  In this case, it was used to determine winning candidate of state congressional election & county turnout.  
Examples:
1. Ballot ID could be checked to confirm no duplicate counts by comparing each individual Ballot against entire list.
2. This data was limited and only included 3 counties and 3 candidates, but the loops used to go through the list is not necessarily limited to this small set.  If election results were available for all 50 states or all counties in a given state, the same logic can still be applied.
3.  Winning candidate in each county.  Rather than just looping through entire list, nested loops would allow us to provide a candidate vote total for each county in the entire list so a breakdown could be provided to see winning candidate in each county versus overall winning candidate.
