# CodeAlpha_YoutubeTrendingVideoAnalysisAndMLModel

CodeAlpha_task

DataSet link - https://www.kaggle.com/datasets/datasnaek/youtube-new 

Analyzed YouTube trending video data to uncover patterns in views, categories, tags, and upload trends. Built a machine learning model to predict video popularity based on key features. This project showcases data cleaning, visualization, feature engineering, and predictive modeling.


PROBLEM STATEMENT

The YouTube Trending Videos dataset contains daily records of videos that reached the trending list across different categories.
However, raw trending data alone does not provide clear insights into:
What type of content trends the most
Which categories dominate the trending page
How views, likes, comments, and engagement vary
Whether some days get higher trending activity
Trends in user interaction (likes/dislikes/comments)
The challenge is to analyze category-wise performance, engagement metrics, daily patterns, and creator trends to help marketers, creators, and analysts understand what drives content virality on YouTube.
This project aims to uncover viewership patterns, engagement behaviour, category strengths, and factors contributing to trending videos.

Task 1 — Data Preprocessing & Feature Engineering
1.1 Data Loading

Imported the dataset in Jupyter Notebook using Pandas:
df = pd.read_csv("USvideos.csv")

1.2 Data Cleaning

 Checked missing values
 
 Dropped unnecessary or duplicate columns
 
 Converted trending_date to datetime format
 
 Cleaned text fields (title, description, tags)

 Handled incorrect datatypes

1.3 Feature Engineering

Created new columns:
 day_of_week → Extracted from trending date

 title_length → Character count

 tags_count → Number of tags

 engagement_rate →
(df['likes'] + df['comment_count']) / df['views']

 like_dislike_ratio

Task 2 — Exploratory Data Analysis (EDA)

Performed analysis on:

 Trending frequency by day of week

 Most popular video categories 

 View distribution

 Like & comment patterns

 Creator-wise analysis

 Engagement distribution across categories


Task 3 — Visualizations

Created meaningful charts such as:

 Trending Videos by Day of Week

 Category-wise video count

 Top 10 Most Viewed Trending Videos

 Likes vs Views scatter plot

 Engagement rate distribution

 Comment count comparison

 Correlation heatmap

These visuals helped understand the platform’s engagement trends.


3.1 Analysis & Insights
3.1.1 Category Performance

 Entertainment dominates the trending list with the highest number of videos.

 Music videos generate the highest views and engagement.

 Sports and News trend less frequently but show high interaction during major events.

3.1.2 Views & Engagement Patterns

 Videos with strong viewer interaction (likes & comments) are more likely to trend.
 
 Some trending videos have millions of views but low engagement, indicating passive audiences (common in music & trailers).

 High engagement rate is seen in categories like Gaming, Commentary, and Vlogs.

3.1.3 Day-Wise Trending Activity

Friday and Saturday show the highest number of trending uploads.

 Monday has the lowest trending activity.

 Engagement peaks during weekends.

3.1.4 Like–Dislike Ratio

 Trending videos generally have a high like ratio.

 Categories such as Politics and News show higher dislike ratios due to polarizing content.

3.1.5 Comment Behaviour

 Videos with more comments show higher community involvement.

 Music and Entertainment videos dominate comment volume.


Task 4: Machine Learning Model
4.1 Objective

 Predict video engagement (views or likes) based on metadata, category, tags, upload time, and other features.

4.2 Model Used

 Linear Regression and Random Forest Regressor for predicting views.

 Accuracy evaluated using RMSE and R² scores.

4.3 Key Features

 category_id, title_length, tags_count, publish_hour, days_trending

 Sentiment polarity score of comments

4.4 Insights from Model

 Category, upload timing, and title length strongly influence engagement.

 Videos with more positive comments tend to have higher views.

 Model predictions help channels optimize content strategy for better trending performance.


Conclusion

This project analyzed YouTube trending videos using views, likes, comments, categories, channels, and sentiment patterns. Key insights include:
 Positive comments dominate, reflecting overall viewer satisfaction.

 Engagement depends on content category, upload timing, and channel influence rather than just subscriber count.

 Machine learning models help predict potential trending success, providing actionable strategies for creators.


 Overall, data-driven content optimization, audience engagement understanding, and predictive modeling can significantly improve YouTube performance.
