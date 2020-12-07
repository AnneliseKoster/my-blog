---
title: Hotel Analysis
author: ~
date: '2020-12-07'
slug: hotel-analysis
categories: []
tags: []
---

## Hotel Analysis

# Introduction
The first dataset I chose was the Hotel Booking Demand dataset from Kaggle.com, this dataset is originally from the article Hotel Booking Demands Datasets, written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019. Thomas Mock and Antoine Bichat are responsible for cleaning the original data. This dataset contains booking information for two hotels but since the hotels mentioned are real hotels any data pertaining to customer or hotel identification has been deleted. By analyzing the data I hope to determine if there is a difference in cancellation rates or lead times between the two hotels as well as determine which month is the busiest for the hotels and determine the respective lead times for each month.


# Exploratory Data Analysis
While performing exploratory data analysis I gained a few insights about the data. Firstly, the dataset only contains data from July 2015 - August 2017 meaning that when looked at on a per year basis 2015 and 2017 will contain less months worth of data, this should be kept in mind when comparing the years to each other. 

, , month = January

              
               2015 2016 2017
  City Hotel      0 1364 2372
  Resort Hotel    0  884 1309


, , month = February

              
               2015 2016 2017
  City Hotel      0 2371 2594
  Resort Hotel    0 1520 1583

, , month = March

              
               2015 2016 2017
  City Hotel      0 3046 3412
  Resort Hotel    0 1778 1558

, , month = April

              
               2015 2016 2017
  City Hotel      0 3561 3919
  Resort Hotel    0 1867 1742

, , month = May

              
               2015 2016 2017
  City Hotel      0 3676 4556
  Resort Hotel    0 1802 1757

, , month = June

              
               2015 2016 2017
  City Hotel      0 3923 3971
  Resort Hotel    0 1369 1676

, , month = July

              
               2015 2016 2017
  City Hotel   1398 3131 3559
  Resort Hotel 1378 1441 1754

, , month = August

              
               2015 2016 2017
  City Hotel   2480 3378 3125
  Resort Hotel 1409 1685 1800

, , month = September

              
               2015 2016 2017
  City Hotel   3529 3871    0
  Resort Hotel 1585 1523    0

, , month = October

              
               2015 2016 2017
  City Hotel   3386 4219    0
  Resort Hotel 1571 1984    0

, , month = November

              
               2015 2016 2017
  City Hotel   1235 3122    0
  Resort Hotel 1105 1332    0

, , month = December

              
               2015 2016 2017
  City Hotel   1654 2478    0
  Resort Hotel 1266 1382    0


Continuing my exploratory analysis I wanted to compare the number of transactions per hotel type for year. When just looking at the below table it looks like the hotels are experiencing a decrease in number of transactions but as mentioned above we need to remember that 2016 is the only year in this dataset that we have a full 12 months of data for.

What the below table can tell us is that the city hotel experiences more transactions than the resort hotel. Without more data we are unable to determine if the larger number of transactions is due to the city hotel being more popular than the resort hotel or if the city hotel is simply bigger than the resort hotel thus having more rooms and more booking transactions or it is possible that guests tend to stay longer at the resort hotel making the city hotel have a faster room turnover making it look busier when in actuality it is simply the number of transactions that is larger.

            
                2015  2016  2017
  City Hotel   13682 38140 27508
  Resort Hotel  8314 18567 13179
  
The last two variables I looked at were lead time and cancellations. I wanted to get a broad idea of what the average lead time (time between booking a reservation and showing up at the hotel) and cancellation rates were. Based on this high-level viewing I saw that the average lead time is 104 days and the average cancellation rate is 37%. 

   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
      0      18      69     104     160     737 
      
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
 0.0000  0.0000  0.0000  0.3704  1.0000  1.0000 
 
 
# Data Analysis & Results

# Question 1
The first question I sought to answer was to determine if there is a difference in cancellation rates between the two types of hotels. I attempted to answer this question by generating a table that grouped the data by hotel type and year and then I took the average of all the data points in that specific section and generated an average of the is_canceled column to determine what the cancellation rate is for that hotel in a given year. Based of the below table we can see that there is a marked numerical difference between the cancellation rate for the city hotel and the one for the resort hotel. The city hotel's cancellation rate has hovered between 40%-43% over the 3 years of data and the resort's cancellation rate has been between 25% and 30% over the same time frame. The cancellation rate for the city hotel has stayed relatively stable across all three years, I did not notice either an increasing or decreasing trend. However for the resort hotel the cancellation rate has been increasing over the three years of data, this is not a long enough time frame to determine if this is actually a trend but it is an interesting observation. 
 
hotel
<fctr>
arrival_date_year
<int>
mean_cancellation_rate_per_year
<dbl>
City Hotel	2015	0.4388247
City Hotel	2016	0.4039591
City Hotel	2017	0.4250036
Resort Hotel	2015	0.2571566
Resort Hotel	2016	0.2655249
Resort Hotel	2017	0.3076106
6 rows


# Question 2
The second question I explored was is there a difference in lead times between the two types of hotels. I sought to answer this question by again generating a table that sorted the data by hotel type and year but then I used lead time as my variable of interest to determine what the average lead time was for each hotel by year. I also generated a box plot so that I could visually see the difference in the data distribution for the two hotel types in regard to lead time. Upon performing these analyses I was able to determine that there is a difference in lead time between the two hotels. The city hotel has a longer lead time than the resort with the mean for the city hotel being approximately 109 days for all three years of data and the mean for the resort being 91 days. Another thing we can see is that the lead times for both hotels has been increasing over the three years of data included in the dataset. 
 
 
 
hotel
<fctr>
arrival_date_year
<int>
mean_lead_time
<dbl>
median_lead_time
<dbl>
City Hotel	2015	105.74682	60
City Hotel	2016	108.09995	71
City Hotel	2017	113.98775	87
Resort Hotel	2015	83.25656	54
Resort Hotel	2016	92.12786	54
Resort Hotel	2017	99.38956	66
6 rows


 
 
 
 
 
 
 
 
 
 


