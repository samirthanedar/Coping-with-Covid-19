# How is the general public coping with Covid-19?

## Overview

Covid-19 needs no introduction. As a country, we are over three months into a scary pandemic. But this has been silently spreading worldwide since December, 2019. Luckily my family and I have been spared from the worst of the disease and we’re all healthy. However, as the infectious disease progressed, I’ve felt strong emotions and worried about the future. Once the government shutdown started, I felt a lack of control and complete uncertainty for what would happen next. Although this was anecdotal, I wondered how others were coping mentally and emotionally with Covid-19. This gets addressed in the media but this is usually something that we all deal with by ourselves and behind closed doors. 


## Objective

My goal here is to use Twitter to understand the public headspace around Covid-19. I have scraped 75,000 tweets from December 1st, 2019 to May 19, 2020 using the GetOldTweets API, performed topic modeling on the resulting corpus, and then analyzed how the topics have changed over time.


## Top 10 Topics

I used TF-IDF to vectorize the data and then NMF for dimensionality reduction. Here are the resulting topics:

1. Initial Chinese Outbreak
1. Trump's response to Covid-19
1. Italy's Covid-19 outbreak
1. Stopping the spread
1. Anger
1. Working from home
1. Cruises and quarantines
1. Wearing a mask
1. White House briefings
1. Second Wave Warnings

## Findings:

From the document-topic matrix taken from the NMF model, I took a sum of each topic column to get a value representing how often that topic was mentioned in the whole corpus. We can call this the "relative importance" of each topic. Then I split up the data by month, so we can see how the relative importance of each topic changed over time.

In December and January, the world is only talking about the Chinese outbreak in Wuhan. In February, people begin to also discuss the outbreak in Italy. As the world starts to worry about stopping the spread, events around the world start to get cancelled. In March, the anger topic reaches it's peak. This topic is largely just people expressing their anger at Covid-19 by using several curse words. By April and May, people have redirected their anger towards Trump and many tweets discuss his handling of the pandemic. Also, new normal topics like working from home and wearing a mask are discussed as well. 

It's interesting to see that solutions such as vaccines and science such as epidemiology are not discussed too much. Many people are angry and choose to focus their thoughts on criticizing others. Also, discussions about a second wave peak in February before the first wave really starts in the U.S. which is strange. Finally, you can see a lot of people dealing with their grief along the same patterns as the 5 stages of grief. The 5 stages of grief is a framework for describing the stages people go through while they are recovering from a loss of a loved one. Many people are dealing with the loss of normal life and are expressing their anger with that.


## Navigating the Project Files:

You should follow the following workflow when going through the notebooks to repeat the results: 
1. Start at 01_data_collection_and_topic_modeling.ipynb to see my experimentation with topic modeling 
1. Next go to 02_topics_per_month.ipynb to see the different topics per month
1. Finally, go to 03_visualization.ipynb to see the visualizations of how the topics changed per month.

I've also included a pickle file of the dataset and the final NMF model to help you reproduce the results.

