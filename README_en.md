 Exploratory Data Analysis Project  
 Video Game Sales – ICE Online Store

This project analyzes historical video game sales to identify what drives a game’s commercial success. We simulate the scenario of December 2016, as the fictional ICE online store prepares marketing strategies for 2017.

The dataset includes sales by region, critic and user scores, platform information, genre, and ESRB ratings.

---

 Project Goals

- Understand trends in video game sales across time and platforms.  
- Identify the key factors associated with successful games.  
- Build regional consumer profiles (North America, Europe, Japan).  
- Test statistical hypotheses about user scores across platforms and genres.  
- Provide actionable insights for marketing strategies in 2017.

---

 1. Dataset Overview

Initial exploration covers:

- Column descriptions  
- Data types  
- Number of games released per year  
- Completeness and reliability of available information  

---

 2. Data Preparation

 Cleaning and standardization
- Rename columns  
- Add/remove/adjust columns as needed  
- Convert data types  
- Document every change and the reason behind it  

 Handling missing values
- Inspect missing values and their meaning  
- Decide whether to fill, drop, or keep them  
- Explain the strategy for each column  

 Feature engineering
- Create a new column containing total global sales (sum of all regional sales)

---

 3. Exploratory Analysis

 3.1 Games released per year  
- Explore annual release volume  
- Check whether each period has meaningful data  

 3.2 Platform performance  
- Compare total sales across platforms  
- Identify platforms that were once popular but declined  
- Observe how long new platforms take to emerge and old ones to disappear  

 3.3 Selecting an appropriate time window  
- Based on previous answers, determine the relevant time period for forecasting 2017  
- Remove older, irrelevant years  

 3.4 Sales by platform  
- Identify leaders and declining platforms  
- Select promising platforms  
- Build boxplots for global sales by platform  
- Compare average sales and distribution differences  

 3.5 Impact of critic/user scores  
- Choose a popular platform (e.g., PS4, Xbox One, 3DS)  
- Build scatterplots comparing scores and sales  
- Calculate correlations and interpret  
- Compare performance of the same games across other platforms  

 3.6 Genre analysis  
- Evaluate the distribution of genres  
- Identify profitable genres  
- Highlight genres with consistently high or low sales  

---

 4. Regional Consumer Profiles (NA, EU, JP)

For each region:

 Top 5 platforms  
- Compare market share across regions  

 Top 5 genres  
- Explain regional preferences  

 ESRB ratings  
- Assess whether rating categories affect sales differently across markets  

---

 5. Hypothesis Testing

 Hypotheses
1. Average user ratings for Xbox One and PC are equal.  
2. Average user ratings for Action and Sports games are different.

 Documentation
- Formulate null and alternative hypotheses  
- Select and justify significance level (alpha)  
- Choose appropriate statistical test  
- Interpret results and their practical meaning  

---

 6. Final Conclusion

Summarize:

- Key drivers of game success  
- Strongest platforms for 2017  
- Most promising genres  
- Regional variations  
- Hypothesis test outcomes  
- Strategic recommendations for the ICE store’s 2017 campaign