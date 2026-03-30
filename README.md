Overview
This is the home page of the competition. Please read the description and the evaluation criteria carefully.

Start

Nov 14, 2025
Close
Dec 8, 2025
Description
In this project, you will participate in a Kaggle competition on retinal image classification. The objective is to develop a machine learning model capable of assessing the severity of diabetic retinopathy from retinal fundus photographs. The fundus, located at the back of the eye, contains the retina, where signs of the disease appear. Your goal is to classify each image into one of the provided ordinal severity levels. Although these distinctions are often subtle and difficult to detect by eye, machine learning models can capture complex, high-dimensional patterns that enable accurate predictions.

To accomplish this task, you are given the following data:

train_data.pkl: This is a pickle file containing both the images and the labels for the training set, within a dictionary. You can open it using the script shown in the following.

test_data.pkl: Another pickle file containing the images of the test set. This time, you can open this file exactly as before, but the dictionary will not contain the key ``labels'' that you will need to predict.

import pickle

# Load the pickle file
with open('path_to_file.pkl', 'rb') as f:
    data = pickle.load(f)

# Access images and labels
images = data['images']
labels = data['labels']
Team Registration (Nov 22nd)
For the graduate section (IFT6390), the task must be solved individually. IFT3395 students can optionally participate in the competition in teams of 2 or 3. Individual participation for both sections is also authorized. In order to participate in the competition, you should:

Create a Kaggle account if you do not have one already.
Enter the competition using the invitation link
From now on, you can access the competition
In the Invite Others section, enter your teammates’ names or team name.
Your teammate has the option to accept your merge.
Fill out the Google form with your team information.
Important note: The maximum amount of submissions is 2 per day, per TEAM. Any team whose individual members have a submission count larger than what is allowed up to-date will be UNABLE to form a team. Example: Today is the first day of competition. A,B,C are three teammates who haven’t formed a team yet.

A submitted 0 times.
B submitted 2 times.
C submitted 1 time.
Because the maximum amount of submissions is 2 per team per day, the total possible submissions for a team is 2. However, the cumulative submission count for A,B,C is 3. Therefore, they will be unable to form a team (They will need to wait for tomorrow, and not submit any submissions for the next day).

First milestone: Beat the baselines (Nov 30th) [50pts]
You can see two baseline scores on the Kaggle leaderboard. You will need to beat both baselines on the public leaderboard in order to get full marks. You may use any method you like, but be mindful that you are working with a small dataset ($<$ 1k examples). Here are some possibilities of methods:

Logistic regression
Decision trees and random forests
Non-linear classifiers such as Kernel Perceptron or Kernel SVM
Important note: In your submission for this milestone, you are NOT allowed to use any machine learning library, e.g. scikit-learn. You should implement your solution from scratch using only NumPy and basic Python functionalities.

Second milestone: Compete (December 8th) [10pts]
In this milestone, you will compete against your peers, and your grade depends on your overall ranking. You are free to implement ANY method you think would work best, and use any library you deem useful, like scikit-learn, Pytorch or Tensorflow.

Important note: The Kaggle leaderboard has a public and private component to prevent participants from “overfitting” to the leaderboard. The public leaderboard shows your score calculated on 50% of the test set, while the private leaderboard is based on your score on the other half of the test set. You are only able to see the public leaderboard during the competition. The points for this phase will be given based on your ranking on the private leaderboard that will be released at the end of the competition.

Important note: You must submit two separate solutions, one for the first phase (beating the baseline), and one for the second phase (your best-performing model). You should name your submission files to distinguish between the two. For your code submission on Gradescope, you should also separate the two solutions.

Third milestone: Submit Code and Report (December 12th) [40pts]
You must write up a report that details your machine learning pipeline, including pre-processing, algorithms, optimization and learning, hyperparameter tuning, and validation procedure. You should also provide and compare the results of other methods you implemented before reaching the best-performing model. The report should include details of the methods used in BOTH the first and second milestones. The report should contain the following elements. You will lose points if you do not follow these guidelines.

Project title
Your team name on Kaggle, as well as the list of team members, including their full name and student number (for graduate students, each team has only one member).
Introduction: briefly describe the problem and summarize your approach and results.
Feature Design: Describe and justify your pre-processing and feature extraction methods.
Algorithms: Give an overview of the learning algorithms used without going into too much detail.
Methodology: Include any decisions about training/validation split, regularization strategy, optimization tricks, setting hyperparameters, etc.
Results: Present a detailed analysis of your results, including graphs and tables where appropriate. This analysis should be broader than just the Kaggle results: include a short comparison of different values for important hyperparameters in your best-performing algorithm and also compare the performance of this method with at least two other methods you implemented. Also, include the results from the method used for Milestone 1.
Discussion: Discuss the pros/cons of your approach and suggest ideas for improvement.
References (very important if you use ideas and methods that you found in some paper or online; it is a matter of academic integrity).
Appendix (optional). Here you can include additional results, more details of the methods, etc.
The main text of the report should not exceed 6 pages. References and appendix can be in excess of the 6 pages. You must submit your code (first and second milestones) and report (third milestone) on Gradescope before December 12th, at 23:59.

Evaluation
The evaluation section describes how submissions will be scored and how participants should format their submissions.

Submission Instructions
You must have separate .py files/notebooks for the first and second milestones. The code must be well-documented. If you are not using Jupyter notebooks, you should include a README file containing instructions on how to run the code. You will need to submit a zip file containing your code and related files to Gradescope.

The prediction file containing your predictions on the test set should only be submitted to Kaggle. Your submission file must be a CSV file with two columns and a header row. IMPORTANT: Make sure your IDs are one-indexed and not zero-indexed as follows:

// sample_submission.csv
ID,Label
1,7
2,5
3,8
...
Evaluation Criteria
Data Competition First Milestone (50 points)

Beat the random baseline model (20 points)
Beat the strong baseline model (30 points)
Data competition Second Milestone (10 points)

Rank above the median (5 points)
Achieve a top-3 ranking on the leaderboard (5 points)
Report (40 points)

You will be graded based on the clarity, depth, and technical soundness of your final report