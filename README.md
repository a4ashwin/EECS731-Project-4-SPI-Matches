# Assignment-Project-4-SPI Match's score prediction
 4th assignment of EECS 731 Intro to Data Science - SPI Match's score prediction

 Prerequisites
Python 3.7.3, Jupyter Notebook, Pandas Library, Numpy Library & sklearn Library

 Introduction:
 In this project, we are going to transform the dataset of SPI matches by using feature engineering. We are going to modify the dataset into a new dataset that has the meaningful data to fit various Regression models so we can make prediction of scores of the teams. We will drop "season", "date", "league_id", "league", "proj_score1", "proj_score2", "xg1", "xg2", "nsxg1", "nsxg2", "adj_score1", "adj_score2" columns as a teams performance should not be dependent on this features of the match in practical scenario. We are going to use team1, team2,	spi1,	spi2,	prob1,	prob2,	probtie,	importance1, and	importance2 as features in predicting the scores. We will be using score1 and score2 as target. team1 and team2 are the features which have the names of the teams. spi is the strength rating of a team at the time of the match which is very important feature in determining the comparative performance of teams against each other. spi1 and spi2 represent the strengths of team1 and team2 respectively. prob1, prob2 and probtie are the probabilities of the teams to win and tie. importance is the measure of overall advantage to a team for a particular match which is calculated on the basis of various aspects like weather, country, field etc. This is an important aspect in predicting the scores as it gives us a sense of advantage any team has on the other.

 Idea:
 To predict the score of individual teams, first, we will be dropping the columns which are not much useful in doing so. We will be using the features team1, team2, spi1, spi2, prob1, prob2, probtie, importance1, importance2, score1, score2. Here, score1 and score2 will be our two targets and we will be using both of them individually to train the models and test them. We will fit the Regression models one by one with the features and then test them to predict a score on the test samples.

 Detailed Process:
 - Download the data from https://projects.fivethirtyeight.com/soccer-api/club/spi_matches.csv
 - Load the dataset into Pandas dataframe from spi_matches.csv
 - Drop the "season", "date", "league_id", "league", "proj_score1", "proj_score2", "xg1", "xg2", "nsxg1", "nsxg2", "adj_score1", "adj_score2" as columns are not significant in predicting the scores of the teams.
 - Drop the rows with Nan(missing values) as they won't help in achieving our goal and also, they will create discrepancies in prediction.
 -  Encode the teams name in team1 and team2 feature as our model will only take numerical values and names will have strings. We will be using LabelEncoder for the same. We will replace the these columnteam1	team2	spi1	spi2	prob1	prob2	probtie	importance1	importance2	score1	score2s with the LabelEncoder columns.
 - Initialize, train, and predict the scores for both the teams using RandomForestClassifier, ExtraTreesClassifier and MLPClassifier Regression models one by one.
 - Save the predictions with the rest of the data and actual scores.

 Result:
 We have successfully used the exploratory data analysis technique to get the idea of the data and remove insignificant data from the original dataset. We have used feature engineering to transform and make a final meaningful dataset for our particular goal. We successfully used the 3 Regression models viz RandomForestClassifier, ExtraTreesClassifier and MLPClassifier to predict the score of the individual teams in a match based on various features. We have got an average of 32% accuracy from RandomForest, 32% from ExtraTrees and 30% from MLPClassifier.


 Built With:
 Jupyter Notebook
 Python 3.7.3
 Pandas
 NumPy

 Authors:
 Ashwin Rathore

 License:
 This project is created for Course EECS 731 Assignment for University of Kansas.
 Acknowledgments
 https://projects.fivethirtyeight.com/soccer-api/club/spi_matches.csv
