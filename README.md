# Vanguard A/B Test UI Project

## 🧠 Introduction
This project analyzes an A/B test conducted by Vanguard, a U.S.-based investment management firm, to evaluate a new user interface (UI) design. The updated UI incorporates in-app onboarding prompts to enhance the online experience.

### Objective
Determine whether the new UI leads to a higher completion rate for users.

---

## 📊 Data

### Datasets Used
- `df_final_demo`: Client demographics (age, gender, tenure)
- `df_final_web_data`, `pt_1`, `pt_2`: Interaction logs (merged)
- `df_final_experiment_clients`: Test/control group assignments

### Main Challenges
- Merging datasets from multiple sources
- Handling missing or unknown gender values
- Interpreting open-ended business questions
- Calculating step-level KPIs across user flows

### Strengths
- Large sample size (50K+ users)
- Balanced demographics across groups
- Detailed interaction logs

### Weaknesses
- ~⅓ of users have unknown gender
- Some ambiguity in defining user behavior steps

---

## ❓ Research Question
**Does the new digital UI increase the process completion rate?**

### Conclusion: ✅ Yes
- **Test Group Completion Rate:** 58.52%
- **Control Group Completion Rate:** 49.84%
- **Uplift:** +8.68% (statistically significant, p ≈ 0)

---

## 🛠️ Methodology

### 1. Data Cleaning & Preparation
- Merged logs and experiment data by client ID
- Standardized formats and category labels
- Created flags for test vs. control groups
- Filtered relevant sessions for KPI analysis

### 2. Exploratory Data Analysis (EDA)
- Analyzed high-frequency users (61–90 visits)
- Profiled top users: Ages **51–83**, tenure **4–30 years**
- **Gender split:** ~33% female, ~34% male, ~33% unknown
- **Tenure peaks** at 5 years, then levels off

### 3. KPI Definitions

#### Completion Rate
- % of users reaching final "Confirm" step
- **Control:** 49.84%
- **Test:** 58.52%
- **Uplift:** +8.68%

#### Time on Step (in seconds)
| Step | Control | Test |
|------|--------|------|
| Step 1 | 52.44 | 55.68 |
| Step 2 | 113.51 | 133.58 |

#### Error Rate
- % of sessions where users backtracked
- **Control:** 88.10%
- **Test:** 92.05%
- **Increase:** +3.95%

### 4. Hypothesis Testing
- **Test Type:** Two-proportion z-test
- **Significance Level:** 5%
- **P-value:** ≈ 0 → Reject null hypothesis
- The test group performed significantly better

---

## ✅ Experiment Evaluation

### Design Quality
- **Control Group Size:** 23,526
- **Test Group Size:** 26,959
- **Gender and tenure are evenly distributed**
- **Random assignment → ✅ No visible bias**
- **Clear hypotheses and consistent KPI definitions**

### Duration Assessment
- **Experiment Period:** 03/15/2017 – 06/20/2017
- By **May 31st, 91.4%** of confirms were already achieved
- **Conclusion:** Could have ended earlier for efficiency

---

## 📈 Tableau Visualizations
- **Dashboard:** Client Demographics 
- **Tool Used:** Tableau Public
- **Metrics:** Gender, age, tenure, KPI comparisons
- https://public.tableau.com/app/profile/aicanizares/viz/vanguard-tableau/demographics-db
---

## 🤝 Teamwork & Project Management

### Collaboration Style
- No Kanban board (due to illness)
- Flexible division of tasks:
  - One team member: EDA & data cleaning
  - Other team member: Hypothesis testing & visualizations
- Regular check-ins and shared problem-solving

---

## 🚧 Challenges & Learnings

### Challenges
- Vague or open-ended business questions
- Designing effective visualizations in Tableau
- Writing Python code for KPI logic

### Solutions
- Focused on relevance to business outcomes
- Trial and error to master visualization tools
- Peer support and documentation

### Key Learnings
- Importance of framing clear, measurable questions
- Confidence with real A/B test data and KPIs
- Enhanced skills in Tableau, Python, and statistical testing

---

## 📌 Conclusions & Recommendations

### Summary
- Top users are older (**51–83**) and long-tenured (**4–30 years**)
- Gender and tenure are balanced

## 📌 Conclusions & Recommendations
Presentation Slides: https://docs.google.com/presentation/d/1D5a0Y2c75aBYtsVgAv4s6HRb2Fc_i7jaJcw-KCVMQP8/edit?usp=sharing
