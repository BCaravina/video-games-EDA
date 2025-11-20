 Exploratory Data Analysis Project  
 Video Game Sales – ICE Online Store

This project analyzes historical video game sales to understand the drivers of commercial success.  
We simulate a December 2016 business scenario in which the fictional ICE online store prepares its strategy for 2017.

The dataset includes sales by region, critic and user reviews, platforms, genres, and ESRB ratings.

---

 Project Goals

- Investigate sales trends over time and across platforms.  
- Identify factors associated with high-performing games.  
- Build regional consumer profiles (North America, Europe, Japan).  
- Test hypotheses involving user and critic ratings.  
- Produce insights to support ICE’s 2017 marketing strategy.

---

 1. Data Dictionary

Below is a clear description of each dataset column, including units and interpretation.

 **Main columns**

| Column | Description | Units / Notes |
|--------|-------------|---------------|
| `name` | Game title | Text |
| `platform` | Platform on which the game was released | e.g., PS4, X360, DS |
| `year_of_release` | Release year | Integer; missing values were removed before conversion |
| `genre` | Game genre | e.g., Action, Sports |
| `na_sales` | Sales in North America | **Millions of USD** |
| `eu_sales` | Sales in Europe | **Millions of USD** |
| `jp_sales` | Sales in Japan | **Millions of USD** |
| `ROW_sales` | Sales in Rest of World | **Millions of USD** |
| `critic_score` | Average critic score | Scale 0–100 |
| `user_score` | Average user score | Scale 0–10; `"tbd"` entries were converted to `NaN` and then replaced by `-1` |
| `rating` | ESRB age rating | E, T, M, etc. |

 **Derived column**
| Column | Description |
|--------|-------------|
| `global_sales` | Sum of all regional sales; unit: **millions of USD** |

---

 2. Data Preparation

 **Cleaning and standardization**
- Column names adjusted to a consistent snake_case format.  
- Conversion of `year_of_release` to integer after removing missing entries.  
- Processing of `user_score`:  
  - `"tbd"` values treated as missing,  
  - converted to `NaN`,  
  - later replaced with placeholder `-1` for numeric conversion.  

 **Missing values**
- `year_of_release`: rows with missing values removed.  
- `user_score`: placeholder approach used to preserve all records.  
- `critic_score` and `Rating`: maintained as `NaN` when unavailable.

 **Feature engineering**
- Creation of `Global_sales` (sum of regional sales).

---

 3. Exploratory Analysis

 3.1 Releases per year  
- Number of games released annually.  
- Identification of stable periods for modeling.  

 3.2 Platform evolution  
- Comparison of total sales by platform.  
- Observation of platform lifecycles.  

 3.3 Time window selection  
- Determining the most relevant historical range for forecasting 2017.  

 3.4 Sales by platform  
- Boxplots for `Global_sales`.  
- Comparison of averages and dispersion across platforms.  

 3.5 Effect of user and critic scores  
- Relationship between scores and sales.  
- Correlation analysis.  
- Cross-platform comparisons of the same titles.  

 3.6 Genre performance  
- Distribution of genres.  
- Identification of the highest-earning genres.

---

 4. Regional Profiles (NA, EU, JP)

For each region:

 Top 5 platforms  
- Differences in market share and consumer behavior.

 Top 5 genres  
- Cultural and stylistic variations among regions.

 ESRB rating influence  
- Whether ratings affect sales differently across markets.

---

 5. Hypothesis Testing

 Hypotheses evaluated
1. Average user scores for Xbox One and PC are equal.  
2. Average user scores for Action and Sports games differ.

 Documentation
- Clear definition of null and alternative hypotheses.  
- Choice of significance level and reasoning.  
- Selection of appropriate statistical test.  
- Practical interpretation of the results.

---

 6. Final Conclusion

Summary includes:

- Key factors behind commercial success.  
- Most promising platforms for 2017.  
- High-potential genres.  
- Relevant regional differences.  
- Hypothesis testing outcomes and their meaning.  
- Strategic recommendations for the ICE store.