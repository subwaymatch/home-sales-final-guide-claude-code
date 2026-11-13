# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```

## 2026-11-13: Report page for two questions (Q1 median by city, Q2 mean vs median gap)

- **Asked:** "Turn index.html into a report page for the college-town home sales data. For now, answer only these two questions, each in its own section with a written answer and a chart: Q1. Which city has the highest median sale price? Show the median sale price of every city. Q2. Using all rows (no price rule), which city's mean sale price is furthest above its median, as a percent of the median? Show the mean and median of every city, and explain in one or two sentences what causes the largest gap." Plus the rules: valid price is $10,000 to $5,000,000 inclusive, Q1 uses valid prices only, city means city and state together, compute every number from the CSV in the page, then commit and open a pull request into main.
- **Agent produced:** A single-page `index.html` that loads `data/college_town_home_sales.csv` in the browser and computes every number on the page: the Q1 median ranking (valid prices), the Q2 mean, median and gap for every city (all rows), and the written answers, which are filled in from those computed values. Each question has a bar chart and a table of every city. The cause sentence for Q2 is written from computed values: Athens, GA has four sales above $5,000,000, and its largest sale adds about $28,802 to the mean.
- **Checked or changed:** I recomputed Q1 and Q2 with a separate Python script that reads the CSV, and the page shows the same figures for every city. The page loads with no console errors. I looked at screenshots of both sections in light and dark mode. The page's counts of 40 sales below $10,000 and 31 above $5,000,000 match the description sheet's figures.
