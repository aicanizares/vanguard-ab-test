Vanguard A/B Test UI Project
🧠 Introduction
This project analyzes an A/B test run by Vanguard, a U.S.-based investment management firm, to evaluate a new user interface (UI) design. The new design includes in-app onboarding prompts to improve the online experience.

Objective:
Determine whether the new UI leads to a higher completion rate for users.

📊 Data
Datasets Used:

df_final_demo: Client demographics (age, gender, tenure)

df_final_web_data, pt_1, pt_2: Interaction logs (merged)

df_final_experiment_clients: Test/control group assignments

Main Challenges:

Merging datasets from multiple sources

Handling missing or unknown gender values

Interpreting open-ended business questions

Calculating step-level KPIs across user flows

Strengths:

Large sample size (50K+ users)

Balanced demographics across groups

Detailed interaction logs

Weaknesses:

~⅓ of users have unknown gender

Some ambiguity in defining user behavior steps

❓ Research Question
Does the new digital UI increase the process completion rate?

Conclusion: ✅ Yes

Test Group Completion Rate: 58.52%

Control Group Completion Rate: 49.84%

Uplift: +8.68% (statistically significant, p ≈ 0)

🛠️ Methodology
1. Data Cleaning & Preparation
Merged logs and experiment data by client ID

Standardized formats and category labels

Created flags for test vs. control groups

Filtered relevant sessions for KPI analysis

2. Exploratory Data Analysis (EDA)
Analyzed high-frequency users (61–90 visits)

Profiled top users: ages 51–83, tenure 4–30 years

Gender split: ~33% female, ~34% male, ~33% unknown

Tenure peaks at 5 years, then levels off

3. KPI Definitions
Completion Rate:

% of users reaching final "Confirm" step

Control: 49.84%

Test: 58.52%

+8.68% uplift

Time on Step (in seconds):

Step 1: 52.44

Step 2: 55.68

Step 3: 113.51

Confirm: 133.58

Error Rate:

% of sessions where user backtracked

Control: 88.10%

Test: 92.05%

+3.95% increase

4. Hypothesis Testing
Test Type: Two-proportion z-test

Significance Level: 5%

P-value: ≈ 0 → Reject null hypothesis

The test group performed significantly better

✅ Experiment Evaluation
Design Quality
Control Group Size: 23,526

Test Group Size: 26,959

Gender and tenure are evenly distributed

Random assignment → ✅ No visible bias

Clear hypotheses and consistent KPI definitions

Duration Assessment
Experiment Period: 03/15/2017 – 06/20/2017

By May 31st, 91.4% of confirms already achieved

Conclusion: Could have ended earlier for efficiency

📈 Tableau Visualizations
Dashboard: Client Demographics

Tool Used: Tableau Public

Metrics: Gender, age, tenure, KPI comparisons
(Dashboard link placeholder: to be updated)

🤝 Teamwork & Project Management
Collaboration Style:

No Kanban board (due to illness)

Flexible division of tasks:

One team member: EDA & data cleaning

Other team member: Hypothesis testing & visualizations

Regular check-ins and shared problem-solving

🚧 Challenges & Learnings
Challenges:

Vague or open-ended business questions

Learning to design effective visualizations in Tableau

Writing Python code for KPI logic

Solutions:

Focused on relevance to business outcomes

Trial and error to master visualization tools

Peer support and documentation

Key Learnings:

Importance of framing clear, measurable questions

Confidence with real A/B test data and KPIs

Enhanced skills in Tableau, Python, and statistical testing

📌 Conclusions & Recommendations
Summary:

Top users are older (51–83) and long-tenured (4–30 years)

Gender and tenure are balanced across groups

New UI led to a +8.68% increase in completion rate

Slight increase in error rate suggests more interaction or complexity

Experiment had solid design and sufficient data

Recommendations:

✅ Deploy the new UI to all users

📉 Reduce backtracking by simplifying long steps (e.g., Step 3)

👴 Improve accessibility for older users

🧪 Shorten experiment duration in future when early trends are conclusive

📊 Monitor for additional KPIs (e.g., satisfaction, churn)

📁 Files in Repository
df_final_demo.csv – Client demographic data

df_final_web_data.csv, pt_1.csv, pt_2.csv – Interaction logs

df_final_experiment_clients.csv – Test/Control group assignments

vanguard_ab_test_analysis.ipynb – Full Python analysis

tableau_dashboard.twbx – Tableau visualization (packaged)

README.md – This project documentation

👩‍💻 Authors
Sarah Maged

Ana Cañizares

📅 Date: May 22, 2025
