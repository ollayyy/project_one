# project_one
This project analyzes team and conference-level trends in the 2022 NBA Regular Season

Code Breakdown
The code takes data from Sportradar's NBA API by looping through each team's statistics in a given season, and stores them in a Data Frame for analysis and vizualisations.

In order to create the loop, we first need a list of team IDs to make the API calls. We wrote a function which takes care of this after the declarations.

Once we have the list of team IDs we can make a for loop which retrieves the desired data from the API's JSON return and adds it to our Data Frame (team_df) for future use.

We then create a similar loop which retrieves info like the team's conference and position in the standings (standing_df), and merge them into last_team_df, which we can then use for further calculations and analysis.

Analysis and Methedology
To assess team strength, we're using Dean Oliver's four factors—effective field goal percentage, turnover rate, offensive rebound rate, and free throw rate—as well as Net rating (points scored per 100 possessions minus ppints allowed per 100 possessions). The four factors will also help us assess stylistic differences between conferences.

Once we create new colummns in last_team_df with all the calculations for the teams, we use groupby to separate the conferences and look for trends using boxplots and scatter plots.

Results
Much of the conventional wisdom about the differences in conference style (the west being more pace and space and offensively oriented, the east being weaker on the margin and more defensively focused) held true.

The weighted sum of Oliver's four factors correlates strongly with winning, but net rating correlates to an even greater degree, justifying its widespread use.
