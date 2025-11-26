# NHANES Inferential Statistics
------
Using NHANES data for inferential statistics

This project uses NHANES 2021–2023 public health survey data to perform inferential statistical analyses to explore relationships or differences between variables from datasets. After cleaning and merging multiple datasets, five research questions were tested using chi-square, t-tests, ANOVA, and correlation.

## Variables Used
### Categorical (recoded)
------
Marital Status (`DMDMARTZ`) → Married / Not married

Education Level (`DMDEDUC2`) → Bachelor+ / Less than bachelor

Vitamin D Interpretation (`LBDVD2LC`) → Normal / Low

Hepatitis B Antibody (`LBXHBS`) → Positive / Negative

Kidney Problems (`KIQ022`) → Yes / No

Continuous (`cleaned`)

Age (`RIDAGEYR`)

Systolic BP (`BPXOSY3`)

Diastolic BP (`BPXODI3`)

Sedentary Minutes (`PAD680`) — removed NHANES placeholders: 7777, 9999

Self-Reported Weight (`WHD020`) — removed placeholders: 7777, 9999

## Analyses
### 1. Marital Status × Education (Chi-Square)
- χ² = 155.64, p < 0.001
- Significant association: higher education linked with being married.
### 2. Marital Status → Sedentary Minutes (T-Test)
- t = –2.76, p = 0.0058
- Significant difference: not married individuals had more sedentary time.
### 3. Age & Marital Status → Systolic Blood Pressure
- Correlation (age → BP): r = 0.509, p < 0.001 → systolic BP increases with age.
- ANOVA (marital status): F = 0.284, p = 0.594 → no difference by marital status.
### 4. Weight ↔ Sedentary Time (Correlation)
- r = 0.156, p < 0.001
- Small but significant positive correlation: heavier individuals spent slightly more time sedentary.
### 5. Vitamin D × Kidney Health (Chi-Square)
- χ² = 0.00, p = 1.0
- No association between vitamin D status and kidney problems.

## Tools Used
- Google Colab
- Python
### Project Dependencies
- `pandas` – data loading, cleaning, recoding
- `numpy` – numeric operations, missing values
- `matplotlib` – plots (boxplots, scatterplots)
- `seaborn` – statistical visualizations
- `scipy` – statistical tests (chi-square, t-test, ANOVA, correlation)


## How to Run
- Upload NHANES `.xpt files` into your working directory from [NHANES 2021-2023 data page from CDC website](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023)
- Run the Python script or Jupyter notebook
- View the printed test results and generated plots
