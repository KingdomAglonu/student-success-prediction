# Student Success Prediction & Retention Strategy

## Overview
In this project, I analyzed student engagement and performance data to understand what drives student dropout in an online learning environment.

The goal of this project is to identify students at risk of dropping out early and provide actionable insights that can improve retention.

## Business Problem
Student retention is a major challenge for online learning platforms. When students disengage early, completion rates decline and learning outcomes suffer.

This project uses engagement and performance data to predict dropout risk and identify the strongest behavioral indicators of non-completion.

## Dataset
I used a public online course engagement dataset from Kaggle.

### Features
- CourseCategory
- TimeSpentOnCourse
- NumberOfVideosWatched
- NumberOfQuizzesTaken
- QuizScores
- CompletionRate
- DeviceType
- CourseCompletion

## Target Variable
I created a binary target variable called `dropout`:
- `1` = student dropped out
- `0` = student completed the course

## Tools Used
- Python
- pandas
- numpy
- matplotlib
- scikit-learn
- Google Colab

## Exploratory Analysis
From the analysis, I found that:
- Students who spend less time on course content are more likely to drop out
- Lower quiz scores are associated with higher dropout risk
- Students who watch fewer videos tend to have lower completion outcomes
- Engagement behavior is a strong indicator of student success

## Modeling Approach
I built a Logistic Regression model to predict student dropout.

### Initial Model
Included `CompletionRate`
- Accuracy: **79.1%**
- Recall for dropout class: **85%**

### Improved Model
Removed `CompletionRate` to reduce leakage
- Accuracy: **74.5%**
- Recall for dropout class: **83%**

Even after removing a leakage-like feature, the model maintained strong performance, showing that engagement and performance data alone can predict dropout risk effectively.

## Key Drivers of Dropout
The strongest predictors were:
- QuizScores
- NumberOfQuizzesTaken
- NumberOfVideosWatched
- TimeSpentOnCourse

This suggests that engagement and performance are the most important signals for student retention.

## Business Recommendations
- Monitor student engagement early in the course
- Provide support for students with low quiz scores
- Encourage consistent participation in videos and quizzes
- Use behavioral activity as an early warning signal for dropout risk

## Conclusion
This project demonstrates that student engagement and performance are strong predictors of course completion.

By identifying at-risk students early, edtech platforms can design targeted interventions that improve retention and learner outcomes.

## Author
**Kingdom Aglonu**  
Data Scientist | Machine Learning | Analytics