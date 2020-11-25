![](https://github.com/Ela-Bo/YouTube_Success_Prediction/blob/main/image.png)
[Image Source](https://pixabay.com/de/photos/kamera-digital-fotografie-isoliert-819359/ )

**In case of sensitive internal data: Please note that the notebooks will be provided as soon as possible after clarification with our stakeholder. [Here](https://github.com/Ela-Bo/YouTube_Success_Prediction/blob/main/Presentation.pdf) you can find a short presentation.**

# YouTube Success is predictable! 
## Utilizing early view patterns to predict the success of a YouTube video with machine learning techniques.

For many people, YouTube plays a part in their daily life. It is one of the **main sources of online video entertainment, education, advertisement, to keep up to date** and much more. So it might not surprise that creators are eager to identify factors that might tweak the performance resp. the **success of an uploaded video**. With the help of Data Science we unleashed not only Data Analytics and Machine Learning on our journey, but even a neural network, trying to find factors that determine a success or even explain it. 

# Data Set
The dataset for this project was provided by Rocket Beans (a Hamburg based company). 
Additionaly, we scraped data from other german YouTube Channels that produce content similar to Rocket Beans e.g. with focus on gaming or movie topics.

# About Rocket Beans
Rocket Beans is an **online platform for digital content** as well as a creative producer and publisher. The YouTube channel Rocket Beans TV was founded in 2012 and it's the first german, indepentend and community-driven 24/7 web channel which started broadcasting on January 15th, 2015.

Every day there is new **content about gaming, digital pop culture and entertainment topics**. Everything started with their core competencies in gaming. Topics such as films, quizzes, sports or cooking are also developed in the rocket bean style.

Rocket Beans are currently online with **4 YouTube channels** and over 1 million subscribers (in total for all 4 channels). In addition to being able to see the content 24 hours a day on the rocketbeans.tv site, the entire program can be heard live on Twitch and YouTube, and all videos are uploaded to the YouTube channels in the end.

# About YouTube
When YouTube first made it's way onto the internet, few people realized how many hours of video we’d be watching years later. Nowadays YouTube counts **two billion logged-in monthly** users worldwide, and ranks as the most widely used online platform among U.S. adults. It’s the world’s second largest search engine and **second most visited site after Google**. But with more than **500 hours of video uploaded every minute**, effective YouTube marketing as well as getting the users attention is easier said than done. So it's very important to take a closer look at YouTube Data.

# Business Case
## What is a successful video?
In the following this is an exploratory data analysis for predicting if a YouTube video is going to be successful or not. 
There are many different ideas and approaches how to assess the success of YouTube - Video:
* Comments to Views: 0.5%
* Likes to Views: 4%
* Views to Subscribers: 14%.

In exchange with Rocket Beans we have decided for: **like-view ratio 4%**
Which basically means, that at least 4% of the views did push the like button.

## The Process
After receiving the first dataset from Rocket Beans and a first EDA we have decided to process with a focus on the both
* The **whole Rocket Beans portfolio** (4 YouTube channels)
* Focus on the famous channel **Rocket Beans TV channel**

# EDA
For the findings and an indepth dive, please consult the resp. notebooks:
* [LINK EDA TOTAL]
* [LINK EDA RBTV]

# Model
## Feature selection and Model building
After the EDA, features for the predictive model have been selected. Some aspects might be highlighted that needed our attention. 
* Due to the risk of **data leakage** most YouTube related features were dropped
* As a first step, we used Random Forest, Logistic Regression, KNN, Decision Tree, Ada Boost and XGBoost with a following feature selection.
* After a **base model**, we conducted feature engineering and grid search to improve our result and build our **final model**

## Thumbnail Success Prediction
Since the thumbnail is actually the first thing what a potential viewer sees of a video, this could give valuable insights. To expand our approach to predict whether a video will excel the 4% like/view-ratio we **conducted an analysis of the Thumbnails of the YouTube videos**
* We've created a **SVM** and a **CNN** to categorize thumbnails into successful (over 4% like/view-ratio) and not successful
* To train our CNN in a better way, we **scraped thumbnails** from several other different german YouTube-Channels
* You can find the notebooks and their results:
  * [Link to SVM notebook]
  * [Link to CNN notebook]
* We even build a **short Web App**, to upload a thumbnail and predict if this might be a success or not. As it's only deployed local, you can only see some screen shots in our presentation.  


# Results - What did we find out?
* The best model that we created was a **Logistic Regression Model**
* With **87% accuracy** it allocated videos correctly in the successful / not successful categories
* The CNN (SVM) categorized Thumbnails of Videos correctly with 75% (73%) into the categories correctly. Unfortunately in case of too few images the CNN is good in finding "not succesful" images but it can't detect "succesful" images well. We need more images for further training (future work) 

# Future Work
* Take impressions and revenue metrics into account
* Comment Analyzing
* Further analysis of individual host-importance 
* Which videos do we not predict correctly and what do we know about them?
* Improve our CNN (more images)

