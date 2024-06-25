# Big-Data-Management
**This project implements a big data management solution involving data exploration, machine learning and graph analysis. The code for this is available in the Big-Data-Management-Notebook.ipynb file.**

**Dataset Identification**
Chosen Dataset: Catch The Pink Flamingo dataset. 
* Multi-user game where aim is to catch pink flamingos as they pop up on a world map.
* Players can play individually to create their own team or, join an existing team.
* Players within a team communicate via a chat board.
* As teams progress through levels, the missions change and increase in complexity.

## Exploratory Data Analysis (with PySpark)
1. The pie chart below shows the proportion of clicks per ad category. It shows that the most popular category for ads that were clicked on was computers and the least was automotive.
![Pie chart to show proportion of clicks per ad category](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20clicks%20per%20ad%20category.png)
   
3. The count plot below shows the amount each item was purchased; the most purchased item was item of id 2. This is likely to be affected by item prices or the use of the item within the game.
![Count plot to show the amount each item was purchased](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20amount%20each%20item%20purchased.png)

4. The count plot below shows how many clicks were clicks on a pink flamingo (1) and how many weren’t (0). Significantly, more clicks were not on a pink flamingo, than the number that were, indicating the difficulty of the game.
![Count plot to show how many clicks were clicks on a pink flamingo (1) and how many weren’t (0)](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20pink%20flamingo%20or%20not%20.png)

5. A bar plot was created to show the most popular platforms. iPhone and Android are significantly more popular than the platform types of Windows, Linux and Mac.
![BAr plot to show most popular platforms](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20most%20popular%20platforms.png)

6. A count plot was created to count the number of teams at each level. The count plot below shows a greater number of teams are at the higher levels, until level 6. Level 7 has a slight decrease, followed by a significant decrease at level 8; this indicates that level 7 and 8 may have increased complexity.
![Count plot to count the number of teams at each level](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20numbers%20of%20team%20at%20each%20level.png)

7. Using the year from the dob column, a scatter plot was created to show the distribution of users’ birth years. The scatter plot indicates an older user base.
![Scatter plot to show the distribution of users’ birth years](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/EDA%20-%20distribution%20of%20users'%20birth%20years.png)

## Data Pre-Processing
Data pre-processing involved:
•	Data integration
•	Data cleaning
•	Data transformations
•	Feature engineering
•	Feature selection

## Machine Learning
Data splitting: 70:30 train-test split. 

### Decision Tree
The confusion matrix below shows how the decision tree classifier predicted each of the three classes in terms of true positives, true negatives, false positives, and false negatives. The decision tree classifier performed significantly better at predicting the 0 class (iPhone class). This is likely to be as much of the data belonged to this class.  
![Confusion matrix for decision tree classifier](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Decision%20Tree%20Confusion%20Matrix.png)

### Random Forest
The confusion matrix below shows how the random forest classifier predicted each of the three classes in terms of true positives, true negatives, false positives, and false negatives. The random forest classifier performed significantly better at predicting the 0 class (iPhone class) than the other two. Again, this is likely to be as much of the data belonged to this class.  
![Confusion matrix for random forest classifier](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Random%20Forest%20Confusion%20Matrix.png)

## Graph Analysis (with Neo4j)
1. Analysing the relationship between Users creating TeamChatSessions.
Analysis the relationship between Users creating TeamChatSessions, is that it is evident that one user will create join and leave a TeamChatSession multiple times.
![Analysing the relationship between Users creating TeamChatSessions](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Graph%20Analysis%20-%20Users%20creating%20TeamChatSessions%20.png)

2. Analysing the relationship between Teams participating in TeamChatSessions.
Analysis on the relationship between Teams participating in TeamChatSessions, is that a team participates in a single TeamChatSession.
![Analysing the relationship between Teams participating in TeamChatSessions](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Graph%20Analysis%20-%20Teams%20participating%20in%20TeamChatSessions.png)

3. Analysing the relationship between Users joining TeamChatSessions.
Analysis on the relationship between Users joining TeamChatSessions, is that multiple users will join a TeamChatSession multiple times. 
![Analysing the relationship between Users joining TeamChatSessions](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Graph%20Analysis%20-%20Users%20joining%20TeamChatSessions.png)

4. Analysing the relationship between Users leaving TeamChatSessions.
Analysis of the relationship between Users leaving TeamChatSessions, is that users will leave (and join) multiple TeamChatSessions, presumably when they move/join teams. 
![Analysing the relationship between Users leaving TeamChatSessions](https://github.com/ShriyaSami/Big-Data-Management/blob/ea2b6fcc97af634d40c62b5e6889040f2f8bc2ad/Graph%20Analysis%20-%20Users%20leaving%20TeamChatSessions.png)
