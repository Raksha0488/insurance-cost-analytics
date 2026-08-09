# insurance-cost-analytics

## Problem
Insurance companies and employers need to understand what actually drives 
healthcare costs so they can price policies fairly and design wellness 
programs that target the right people. I wanted to look at real insurance 
data and figure out which personal factors (lifestyle, age, location) 
actually move the needle on cost, and by how much.

## Dataset
Medical Cost Personal Dataset (Kaggle, by Miri Choi) — 1,338 records with 
age, sex, BMI, children, smoker status, region, and insurance charges. 
[View dataset](https://www.kaggle.com/datasets/raksharajput0488/medical-insurance)

## Approach
- Explored the data (it was already fairly clean, no missing values at all) 
  and created BMI category (Underweight/Normal/Overweight/Obese) and age 
  group buckets to make the analysis easier to read
- Used SQL to compare average charges across smoking status, BMI category, 
  age group, and region individually
- Went one step further and looked at smoking status combined with BMI 
  category together, and then all three factors combined (smoker + BMI + 
  age group), to see if these factors compound each other
- Calculated the actual dollar gap between smokers and non-smokers, and 
  estimated the total cost difference this represents across the dataset
- Built a Power BI dashboard to visualize all of this

## Key Findings
Out of 1,338 records, the overall average insurance charge was $13,270. 
Smoking status turned out to be by far the strongest single driver of cost 
— smokers had an average charge of $32,050 compared to $8,434 for 
non-smokers, a gap of about $23,616 per person. Across all 274 smokers in 
the dataset, this gap represents an estimated $6.47 million in additional 
charges compared to if they had non-smoker-level costs. When I looked at 
smoking combined with BMI category, the effect compounded sharply — obese 
smokers averaged $41,558 in charges, nearly double the average for smokers 
overall and almost 5x the overall dataset average. Breaking it down further 
by age too, obese smokers aged 55+ had the single highest average charge of 
any segment at $46,980, while the lowest-cost segments were consistently 
non-smokers regardless of BMI or age. Age on its own showed a fairly steady 
upward trend (from $9,011 for 18-24 year-olds to $18,513 for 55+), and 
region showed comparatively small differences ($12,347-$14,735 across all 
four regions).

## Recommendation
Since smoking status, especially combined with obesity is clearly the 
dominant cost driver, far outweighing age or region, I'd recommend insurers 
or employers prioritize smoking cessation and weight management programs 
specifically for obese smokers rather than spreading wellness budgets evenly 
across all policyholders. Given that this single segment (obese smokers) 
carries by far the highest average cost, even modest improvement here would 
likely have more impact than broader, unfocused wellness initiatives.

## Repository Contents
- `notebook.ipynb` — SQL queries, data prep, and savings calculation
- Dashboard screenshots (smoker, BMI, age, region, combined view)
- `notes.md` — process notes and business questions

## Tools Used
SQL, Python (pandas), Power BI, Excel
