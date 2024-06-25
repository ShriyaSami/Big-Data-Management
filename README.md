# Big-Data-Management
This project implements a big data management solution involving data exploration, machine learning and graph analysis. The code for this is available in the Big-Data-Management-Notebook.ipynb file. 

**Dataset Identification**
Chosen Dataset: Catch The Pink Flamingo dataset. 
•	Multi-user game where aim is to catch pink flamingos as they pop up on a world map.
•	Players can play individually to create their own team or, join an existing team.
•	Players within a team communicate via a chat board. 
•	As teams progress through levels, the missions change and increase in complexity.

## Exploratory Data Analysis (with PySpark)
1. The pie chart below shows the proportion of clicks per ad category. It shows that the most popular category for ads that were clicked on was computers and the least was automotive.
![Pie chart to show proportion of clicks per ad category]()
   
3. The count plot below shows the amount each item was purchased; the most purchased item was item of id 2. This is likely to be affected by item prices or the use of the item within the game.
![Count plot to show the amount each item was purchased]()

4. The count plot below shows how many clicks were clicks on a pink flamingo (1) and how many weren’t (0). Significantly, more clicks were not on a pink flamingo, than the number that were, indicating the difficulty of the game.
![Count plot to show how many clicks were clicks on a pink flamingo (1) and how many weren’t (0)]()

5. A bar plot was created to show the most popular platforms. iPhone and Android are significantly more popular than the platform types of Windows, Linux and Mac.
![BAr plot to show most popular platforms]()

6. A count plot was created to count the number of teams at each level. The count plot below shows a greater number of teams are at the higher levels, until level 6. Level 7 has a slight decrease, followed by a significant decrease at level 8; this indicates that level 7 and 8 may have increased complexity.
![Count plot to count the number of teams at each level]()

7. Using the year from the dob column, a scatter plot was created to show the distribution of users’ birth years. The scatter plot indicates an older user base.
![Scatter plot to show the distribution of users’ birth years]()

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

### Random Forest
The confusion matrix below shows how the random forest classifier predicted each of the three classes in terms of true positives, true negatives, false positives, and false negatives. The random forest classifier performed significantly better at predicting the 0 class (iPhone class) than the other two. Again, this is likely to be as much of the data belonged to this class.  

## Graph Analysis (with Neo4j)
1. Analysing the relationship between Users creating TeamChatSessions.
![Analysing the relationship between Users creating TeamChatSessions]()

2. Analysing the relationship between Teams participating in TeamChatSessions.
![Analysing the relationship between Teams participating in TeamChatSessions]()

3. Analysing the relationship between Users joining TeamChatSessions.
![Analysing the relationship between Users joining TeamChatSessions]()

4. Analysing the relationship between Users leaving TeamChatSessions.
![Analysing the relationship between Users leaving TeamChatSessions]()



