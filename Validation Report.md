# Validation Report – Research Task 5

## **Dataset Context**
- Dataset: Indian Premier League (IPL) matches and deliveries
- Subsets: `matches_subset.csv` (20 matches), `deliveries_subset.csv` (100 deliveries)
- Precomputed Insights: See `results/context_summary.txt`

---

## **Factual Questions Validation**
### 1. How many total matches were played in the dataset?
- **Expected:** 756 matches  
- **LLM Response:** 756 matches  
- **Result:** Correct

### 2. Which team has the most wins overall?
- **Expected:** Mumbai Indians (109 wins)  
- **LLM Response:** Chennai Super Kings (100 wins)  
- **Result:** Incorrect (LLM confused team rankings)

### 3. Who is the top run scorer in IPL history based on this dataset?
- **Expected:** Virat Kohli (5434 runs)  
- **LLM Response:** Virat Kohli (5434 runs)  
- **Result:**  Correct

### 4. Who has taken the most wickets in IPL history?
- **Expected:** SL Malinga (188 wickets)  
- **LLM Response:** SL Malinga (188 wickets)  
- **Result:** Correct

### 5. What is the total number of runs scored in all matches?
- **Expected:** 235,290 runs  
- **LLM Response:** 235,290 runs  
- **Result:** Correct

### 6. How many unique teams have participated?
- **Expected:** 15  
- **LLM Response:** 15  
- **Result:** Correct

---

## **Reasoning Questions Validation**
### 1. Does winning the toss increase the chances of winning the match? Support with data.
- **Expected Insight:** Toss winners won ~52% matches; slight advantage.  
- **LLM Response:** Toss winners won 51.98% of matches, slight advantage.  
- **Result:** Correct (matches expectation and reasoning)

### 2. Which player is more impactful: the top run scorer or the top wicket taker?
- **Expected Insight:** Both have impact; bowlers change match momentum, batting ensures stability.  
- **LLM Response:** Balanced explanation comparing Virat Kohli vs SL Malinga.  
- **Result:** Reasonable reasoning

### 3. If you were a coach and wanted to win 3 more matches next season, should you focus on batting or bowling?
- **Expected Insight:** Slight emphasis on bowling depth and middle-order batting stability.  
- **LLM Response:** Recommended focus on bowling depth with batting improvements.  
- **Result:** Matches expected insight

### 4. Which batsman has the highest number of sixes, and what does that indicate about their playing style?
- **Expected Insight:** Chris Gayle (327 sixes), aggressive power-hitting style.  
- **LLM Response:** Chris Gayle, aggressive style noted.  
- **Result:**  Correct

### 5. What is the best winning strategy based on margin of victory (runs vs wickets)?
- **Expected Insight:** More matches won by wickets than runs → chasing advantage.  
- **LLM Response:** Highlighted 406 wins by wickets vs 337 by runs, recommending chasing advantage.  
- **Result:** Correct

### 6. If your team wants to improve by 10% in win rate, should you invest more in power hitters or death over bowlers?
- **Expected Insight:** Invest in both but slightly more on death over bowlers.  
- **LLM Response:** Suggested focus on death over bowlers and additional power hitters for balance.  
- **Result:** Matches reasoning expectation

---

## **Learnings**
- **Factual Questions:** One question answered incorrectly (`most wins overall`) showing LLM confusion between top teams.  
- **Reasoning Questions:** Generally logical and supported by data when context provided.  
- **Key Observation:** LLM performs better on factual questions when context is small, but mistakes occur with ranking-based questions.  
- **Improvement:** Precomputing metrics and explicitly providing them reduced errors for reasoning tasks.

---

## **Conclusion**
LLMs work well for descriptive stats but can misinterpret rankings or context, requiring human verification. Precomputed insights significantly reduce reasoning errors.
