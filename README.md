# **Kickstarting with Excel**

## **Overview of Project**

### **Purpose**

The purpose of this analysis is to provide a comprehensive review of the performance of other “Play” projects on Kickstarter, specifically with regards to the success of these projects relative to their launch dates. Louise contacted us after her Kickstarter-funded play Fever almost met its fundraising goal over a short period of time, with the intent of analyzing other similar campaign funding goal outcomes relative to their launch dates

To assist Louise, we created the following visualizations with data obtained from Kickstarter’s APIs:

- A Line Chart visualizing the number of successful, failed, and cancelled Kickstarter Projects within the “Theater” category based on the launch months of the projects (data was obtained from 2009 through 2017). See "Analysis of Outcomes Based on Launch Date" below for additional information.

- A line chart plotting the percentage of successful, failed and cancelled projects based on the initial funding goals of each project (utilizing data obtained from 2009 through 2017). See "Analysis of Outcomes Based on Goals" below for additional information.

## **Analysis and Challenges**


### *Analysis of Outcomes Based on Launch Date*


![Analysis_Based_on_Launch_Date](https://github.com/lstanczyk90/kickstarter-analysis/blob/5de77439bfe5e32f05e5516c2ed1b739be957ece/Resources/Theater_Outcomes_vs_Launch.png)


Per review of the above-referenced visualization, we noted that Kickstarter Projects under the “Theater” category were most successful when launched in the months May and June. Conversely, failed projects were more linear in their success rates, but with a notable spike in failed projects that launched in October. As such, our analysis yields that the best time to launch a theater funding project is within Q2.


### *Analysis of Outcomes Based on Goals*


![Analysis_Based_on_Goals](https://github.com/lstanczyk90/kickstarter-analysis/blob/5de77439bfe5e32f05e5516c2ed1b739be957ece/Resources/Outcomes_vs_Goals.png)


Generally, our analysis of the “plays” subcategory yielded that the higher the funding goal, the lower the percentage of successful outcomes (with the exception of funding goals within the range of $35,000 to $44,999). As such, our recommendation is to create a funding goal anywhere from $1,000 to $10,000 (depending on the needs of the project, as goals that exceed the $10,000 have a higher likelihood of failure. 

### *Challenges and Difficulties Encountered*


The primary challenge of this project was “cleaning” the data obtained from Kickstarter’s APIs. Specifically:

- Information like dates were presented in Unix Time, which had to be converted to a standard time format in order to facilitate the visual analysis. This was performed via an Excel function;

- The data obtained from Kickstart was voluminous and included superfluous information that would not be relevant to the goals of this project, as stated within the Overview section above. To standardize this data, we relied on pivot tables and conditional functions to primary focus our analysis on the Theater and Plays category and sub-category, respectively.


## **Results**

- What are two conclusions you can draw about the Outcomes based on Launch Date?

    With regards to Outcomes Based on Launch Date, our above analysis yielded that most successful projects within the Theater category tend to be launched in Q2. Additionally, the analysis indicates that project failures are not as related to launch date, as failures are more linear within the above-referenced visualization. October, however, did experience a sharp spike in failures, thereby indicating that October may not be the best month to launch a new project.

- What can you conclude about the Outcomes based on Goals?

    With regards to Outomes Based on Goals, our analysis generally indicates that the higher the goal, the lesser the rate of success (with the exception of certain outliers, see limitations below for additional information). As such, it is recommended that projects with the "Plays" category include goals o $1,000 to $10,000. Please note, however, that the likelihood of success diminishes as the project goal increases. 

- What are some limitations of this dataset?

    - **Theater Outcomes Based on Launch Date**: As noted within the visualization and above analysis of the results, there tend to generally be more successful projects than failed projects during any given month. As a result, the spike in successful projects in the month of June may be the result of more projects simply being launched in that month than any other factors (as such, the results may present a false positive). Notably, our analysis indicated that projects launched in May and June accounted for approximately 23% of all projects launched during a 12-month period. In other words, our analysis yielded that May and June did indeed have the greatest number of projects launched. An alternative suggestion for future reference would be to create a graph uses weighting techniques to normalize the data for the number of launched projects in order to create a better and more meaningful visualization.

    - **Outcomes Based on Goals**: While our analysis yielded a definitive conclusion, it is worth nothing that there are outliers within the data. Specifically, those projects that launched within the aforementioned $35,000 to $44,999 range did “buck the trend” and experience a higher success rate. Per our analysis, however, only 9 successful projects out of a total of 1,047 overall projects were launched within that range, and only 3 failed projects were launched in that range (for a total of 11 projects out of 1,047, or 0.10%). As such, it is not advisable to try to glean any information from this, as these successful projects may simply be outliers.
    
        Additionally, it is also crucial to consider currency and exchange rates within this analysis. As the analysis simply plots goals (in currency terms) against success rates, it is important to note that currencies with an unfavorable exchange rate relative to the US dollar may skew the results. For example, within the the aforementioned range, one of the Plays that was listed with a goal of 38,000 (specifically, ID#: 2857) was denominated in Mexican Pesos, which results in a lesser amount in USD. 

- What are some other possible tables and/or graphs that we could create?

    Perhaps a more meaningful alternative to the "Outcomes Based on Goals" visualization would be one that is limited to projects with a specific region, in order to standardize the currency. Additionally, with regards to it would also be advisable to plot Outcomes Based on the Percentage Funded of each project in lieu of goals, 