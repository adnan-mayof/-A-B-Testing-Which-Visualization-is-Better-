# A/B Testing: Which Visualization is Better?

## Bar Chart vs. Line Chart

This project uses an A/B experiment to test whether participants are better
able to answer a data-interpretation question when the same information is
presented as a **bar chart** or a **line chart**.

The experiment randomly assigns participants to one of two visualization
conditions.

### Condition A

Bar chart

### Condition B

Line chart

Participants then answer the same visualization question.

Their actual answer is recorded, and the answer is evaluated as correct or
incorrect.

---

# Research Question

> Does visualization type affect whether participants correctly answer the
> visualization task?

More specifically:

> **Do participants answer the task correctly more often when they see a bar
> chart or when they see a line chart?**

---

# Why this is an A/B test

An A/B test compares two versions of something while attempting to keep other
important factors constant.

In this experiment:

**A = Bar chart**

**B = Line chart**

The underlying data and task remain the same.

The visualization format is the experimental manipulation.

Participants are randomly assigned to a condition.

---

# Experiment Workflow

Research Question
        ↓
Problem Definition
        ↓
Hypothesis
        ↓
A/B Visualization Design
        ↓
Sample Size Calculation
        ↓
Sample Size Trade-off
        ↓
Online Participant Recruitment
        ↓
Random Assignment
        ↓
Participant Sees Bar or Line Chart
        ↓
Participant Gives Answer
        ↓
Response Collection
        ↓
Google Sheet:
"Reddit A/B Visualization Experiment"
        ↓
Data Quality Checks
        ↓
Answer → Correct / Incorrect
        ↓
Statistical Analysis
        ↓
Effect Size + Uncertainty
        ↓
Visualization of Results
        ↓
Research Report
        ↓
Decision

---

# The Experiment

## Experimental question

Which visualization produces a higher rate of correct answers?

| Condition | Chart |
|---|---|
| A | Bar chart |
| B | Line chart |

---

# Participant Response

Participants provide an answer to the visualization task.

Example:

Answer:

`September`

The answer is compared with the predefined correct answer.

If the answer matches:

`Correct = TRUE`

If the answer does not match:

`Correct = FALSE`

---

# Primary Outcome

The primary outcome is whether the participant's answer is correct.

The primary metric is therefore the **correct-answer rate**.

For each chart condition:

Correct-answer rate =
Correct responses / Valid responses

The primary comparison is:

Line-chart correct-answer rate
minus
Bar-chart correct-answer rate

---

# Example

Suppose:

Bar chart:

70 correct out of 100 valid responses

= 70% correct

Line chart:

80 correct out of 100 valid responses

= 80% correct

Estimated difference:

80% - 70% = +10 percentage points

The line-chart condition would have a 10-percentage-point higher correct-answer
rate in this example.

---

# Metrics

## Primary metric

Correct-answer rate.

## Secondary metrics

If collected:

- Response time
- Confidence
- Completion rate

Secondary metrics are supporting evidence and do not replace the primary
outcome.

---

# Sample Size

The sample size is planned before recruitment.

The calculation considers:

- Baseline correct-answer rate
- Minimum detectable difference
- Statistical significance level
- Statistical power
- Allocation between chart conditions

See:

`02_experiment_design/sample_size.md`

---

# Sample Size Trade-off

A larger sample generally provides more precise estimates and greater ability
to detect smaller effects.

However, larger samples require:

- More participants
- More recruitment
- More time
- More data processing

A smaller sample is easier to collect but produces greater uncertainty.

The goal is therefore to collect a sample large enough to detect a meaningful
difference while remaining feasible.

See:

`02_experiment_design/sample_size_tradeoffs.md`

---

# Data Source

Participant responses are collected through the experiment and stored in:

**Google Sheet: Reddit A/B Visualization Experiment**

The dataset contains:

- Timestamp
- Anonymous participant ID
- Group
- Chart
- Answer
- Correct
- Event

---

# Example Data

| Timestamp | Participant ID | Group | Chart | Answer | Correct | Event |
|---|---|---|---|---|---|---|
| 10/7/2026 3:45:43 | anonymous | A | bar | September | TRUE | response |
| 10/7/2026 4:30:07 | anonymous | B | line | September | TRUE | response |

---

# Statistical Analysis

The primary analysis compares the proportion of correct answers between the
bar-chart and line-chart conditions.

The analysis reports:

- Sample size
- Number correct
- Correct-answer rate
- Difference in rates
- Effect size
- Confidence interval
- Statistical test
- P-value

The p-value is not interpreted by itself.

The size and uncertainty of the effect are also considered.

---

# Decision

The final decision considers:

1. Direction of the effect
2. Size of the effect
3. Confidence interval
4. Statistical evidence
5. Practical importance
6. Data quality

A statistically significant result is not automatically considered
practically important.

---

# Limitations

Potential limitations include:

- Online participant recruitment
- Non-representative sample
- Self-selection
- Limited task type
- Possible learning or familiarity effects
- Sample-size limitations
- Results may not generalize to every visualization task

---

# Reproducibility

The analysis code and documentation are contained in:

`12_reproducibility/`

The goal is for another person to understand how the result was produced from
the collected data.

---

# Project Structure

The repository follows the complete experimentation lifecycle:

01. Research question
02. Experiment design
03. Visualization design
04. Participant recruitment
05. Experiment execution
06. Data
07. Data quality
08. Statistical analysis
09. Results
10. Figures
11. Research report
12. Reproducibility
