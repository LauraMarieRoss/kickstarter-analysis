# Kickstarting with Excel

## Overview of Project
  The purpose of this challenge was to take Kickstarter data and analyze the relationship between financial goals and ultimate outcome of the project (success, failure, or cancellation of the Kickstarter campaign). Specifically, we looked at theater productions and plays. 
## Analysis and Challenges
  The analysis was split into two parts: An analysis based on Launch Dates and an analysis based on Goals.
### Analysis of Outcomes Based on Launch Date
    First, we used a pivot table to look at theater project months and outcomes (success, failure, or cancellation) with an additional filter for the year the project was created. The initial Kickstarter campaign dates were saved in UNIX code, so a compound formula was used to convert that date style into a readable date recognized by Excel. That formula was =(((J2/60)/60)/24)+DATE(1970,1,1). J2 references the column and row where the UNIX date the Kickstarter was launched resided. This formula is based on understanding that all UNIX dates are calculations where the start of the calendar is January 1, 1970. A column extracting the year of the project’s creation was also created to allow for easy filtering by year. Once the pivot table was created, a simple line pivot chart was also created which plotted lines for counts of success, failure, and cancellation based on the month the campaign began.
### Analysis of Outcomes Based on Goals
    The second analysis was specifically of the subcategory Plays within the Theater parent category. Using the COUNTIFS function we gathered counts based on the specific criteria of plays, outcomes, and financial goal ranges. COUNTIFS is a useful formula for calculating numbers of records that meet specific sets of criteria. We further used the SUM formula and basic division to calculate the percentage of plays that were successful, failed, or cancelled based on their financial goal ranges. That information was then plotted in a basic line chart to make the information easier to interpret.
### Challenges and Difficulties Encountered
     I did not encounter any challenges while completing this analysis. The class materials provided ample guidance, and many references exist for understanding pivot tables and common Excel formulas in addition to what was provided in the educational modules.
## Results
- What are two conclusions you can draw about the Outcomes based on Launch Date?
  May is the month a theater Kickstarter is most likely to succeed. April – July is the best range of months to launch a theater Kickstarter.
- What can you conclude about the Outcomes based on Goals?
  Kickstarter play goals of less than $5000 are most likely to succeed, with a likelihood of 73% or more of being successful. 69% of Kickstarter’s play campaigns have goals of $5000 or less. The second likeliest goal range for success is between $35000 to $44999. Campaigns within this range had a 63% likelihood of success, although this range accounts for only 0.9% of Kickstarter’s play campaigns.
- What are some limitations of this dataset?
  Our analysis did not include likelihood of success based on factors like social media campaigns, population demographics, income medians for the local populations most likely to participate in funding the campaign, or wider information about theater productions in the campaign area. The data set was limited to only Kickstarter campaigns, not the wider understanding of theater production numbers and funding outside of Kickstarter.
- What are some other possible tables and/or graphs that we could create?
  Additional analysis can be done by relating Kickstarter campaign likelihood of success to it being spotlighted by Kickstarter, whether the campaign was a staff pick, and by the country of the campaign.