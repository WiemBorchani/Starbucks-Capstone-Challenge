# Starbucks-Capstone-Challenge
Udacity Data Scientist Nanodegree Capstone Project

## Install

This project requires Python 3.x and the following Python libraries installed:
-NumPy
-Pandas
-matplotlib
-scikit-learn
## Dataset overview
The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers. People produce various events, including receiving offers, opening offers, and making purchases. As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded. There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels. The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.

## Problem Statement

As stated above, the problem statement I am aiming to answer are to Discover customer attributes and buying behaviour , and  how much someone will spend based on demographics and offer type. 

Using the data provided, I answer the above first question using charts for (Demographic data for each customer) and the second question using 3 classification supervised machine learning models, feeding in the data from three combine data (portfolio, profile, Transactional).

## Data used 
### profile.json

Rewards program users (17000 users x 5 fields)
gender: (categorical) M, F, O, or null
age: (numeric) missing value encoded as 118
id: (string/hash)
became_member_on: (date) format YYYYMMDD
income: (numeric)

### portfolio.json

Offers sent during 30-day test period (10 offers x 6 fields)
reward: (numeric) money awarded for the amount spent
channels: (list) web, email, mobile, social
difficulty: (numeric) money required to be spent to receive reward
duration: (numeric) time for offer to be open, in days
offer_type: (string) bogo, discount, informational
id: (string/hash)

### transcript.json

Event log (306648 events x 4 fields)
person: (string/hash)
event: (string) offer received, offer viewed, transaction, offer completed
value: (dictionary) different values depending on event type
offer id: (string/hash) not associated with any "transaction"
amount: (numeric) money spent in "transaction"
reward: (numeric) money gained from "offer completed"
time: (numeric) hours after start of test

### Results

The test data set accuracy of 0.929 and F1-score of 0.931 suggests that the random forest model did not overfit the training data.

