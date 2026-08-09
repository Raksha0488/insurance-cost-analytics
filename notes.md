PROJECT NOTES — Insurance Cost Analysis

Dataset: Medical Cost Personal Dataset (Kaggle, originally by Miri Choi), 
1,338 records. Each row is one insurance policyholder with their age, sex, 
BMI, number of children, smoker status, region, and insurance charges.

What I was trying to figure out:
1. Does smoking status affect insurance charges, and by how much?
2. Does BMI category relate to charges?
3. How do charges vary by age group?
4. Is there a regional cost difference?

Cleaning the data:
This dataset was already quite clean, no missing values in any column. 
I created two new columns to make the analysis easier: bmi_category 
(Underweight/Normal/Overweight/Obese based on standard BMI ranges) and 
age_group (18-24, 25-34, 35-44, 45-54, 55+).

What I found:
Overall average charge across all 1,338 people was $13,270. Smoking status 
was by far the biggest driver of cost, smokers averaged $32,050 compared 
to $8,434 for non-smokers, a gap of about $23,616 per person. Across all 
274 smokers in the data, this works out to roughly $6.47 million in extra 
charges compared to if they had non-smoker-level costs.

When I combined smoking status with BMI category, the effect got even more 
extreme — obese smokers averaged $41,558, way higher than smokers overall 
($32,050) or obese non smokers ($8,843). Breaking it down by age too, obese 
smokers aged 55+ had the single highest average charge in the whole dataset 
at $46,980.

Age on its own showed a steady increase (from $9,011 for 18-24 year-olds 
up to $18,513 for 55+), but nowhere near as dramatic as the smoking effect. 
Region differences were fairly small, averages ranged from $12,347 to 
$14,735 across the four regions, so region doesn't seem to matter nearly 
as much as smoking or BMI.

What I'd recommend:
Since smoking combined with obesity is clearly the biggest cost driver by 
far, it makes more sense for insurers/employers to focus wellness budgets 
specifically on that group (smoking cessation, weight management programs) 
rather than spreading resources evenly across everyone, since that segment 
is where the cost impact is concentrated.
