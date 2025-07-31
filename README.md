# Task 05 – Descriptive Statistics & LLM Analysis (IPL Dataset)

## **Overview**
This repository contains an analysis of the Indian Premier League (IPL) dataset using descriptive statistics and evaluates how Large Language Models (LLMs) (e.g., ChatGPT, Claude, CoPilot) respond to natural language queries derived from the dataset.

The purpose of this research task:
- Generate descriptive statistics from IPL matches and deliveries datasets.
- Design factual and reasoning-based natural language questions.
- Evaluate LLM responses using a smaller dataset subset and pre-computed insights.

---

## **Dataset**
- **matches.csv** – Contains match-level data such as teams, venues, and results.
- **deliveries.csv** – Ball-by-ball delivery data.
- **matches_subset.csv** & **deliveries_subset.csv** – Small subsets provided to LLMs to avoid large context size.

---

## **Descriptive Statistics**
Key insights pre-computed:
- Toss winner won **51.98%** of matches.
- Top run scorer: **V Kohli (5434 runs)**.
- Top wicket taker: **SL Malinga (188 wickets)**.
- Batsman with most sixes: **CH Gayle (327 sixes)**.
- Matches won by runs: **337**, by wickets: **406**.
- Average runs per match: **311.23**.
- Average wickets per match: **11.69**.

For full details, see [`results/context_summary.txt`](results/context_summary.txt).

---

## **Prompts**
Two sets of prompts were designed to test LLM performance:
1. **Factual Questions** – directly verifiable from dataset.
   - See [`prompts/factual_questions.txt`](prompts/factual_questions.txt)
2. **Reasoning Questions** – require context interpretation and decision-making.
   - See [`prompts/reasoning_questions.txt`](prompts/reasoning_questions.txt)

---

## **LLM Analysis**
A notebook [`LLM_Analysis.ipynb`](LLM_Analysis.ipynb) contains:
- Dataset loading and visualization.
- Prompting LLMs.
- Capturing responses.
- Validating results.

Outputs are recorded in:
- **`results/LLM_responses.md`** – Raw model responses.
- **`results/validation_report.md`** – Notes on correctness and reasoning gaps.

---

## **Visualizations**
Two key charts have been generated:
- **Top 5 Run Scorers** <img width="800" height="500" alt="top_batsmen" src="https://github.com/user-attachments/assets/d2907ca7-1a54-4e58-b025-503ccb123454" />
`)
- **Top 5 Wicket Takers** <img width="800" height="500" alt="top_bowlers" src="https://github.com/user-attachments/assets/206a8fd6-c2a5-43e3-84ee-0421d0aedf6e" />
`)

---

## **How to Reproduce**
1. Clone this repository:
   ```bash
   git clone <repo-url>
   cd <repo-folder>
