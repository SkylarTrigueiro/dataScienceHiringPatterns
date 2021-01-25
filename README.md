# Data Science Hiring Patterns

## Table of Contents
* [Overview](#overview)
* [Data?](#Data)
* [Job Growth](#Job-Growth)
* [Salary](#Salary)
* [Locations](#Locations)
* [Big Companies](#Big-Companies)
* [References](#References)

## Overview

This project has two purposes. First, I would like to see what effect COVID-19 has had on data science job hiring in 2020. Second, I would like to gather some insight on when and where recent graduates should look in order to get their first job.

## Data

The data for this project was scraped from the website h1bdata.info using a webscraper that can be found on the following github page: https://github.com/mingen-pan/Scraping-H1B-visa-info (Thank you Mingen Pan!). The data consists of an individuals employer, location by state and city, salary, and the date that the offer was submitted.

## Job Growth

In this section, we will explore how job growth for data science has changed over time and where to look for jobs by state. To start our exploration we will start with the following plot that shows the number of jobs filled by year and quarter.

![](images/barChartJobsFilledByYearAndQuarter.png)

Ignoring the year 2020 for now, you'll notice that hiring spikes in the first quarter of every year and remaing positions are evenly split between the remaining quarters of the year. The spike in positions filled in the first quarter account for approximately 60% of all jobs filled in each given year. It is also clear that the number of positions filled each year has been increasing each year. Things obviously change when we look at when jobs are filled in 2020. A lot more positions have been filled in the second quarter compared to the previous years.

Since I only have data for the first three quarters of 2020, I will now verify that hiring has slowed down by looking at the total jobs hired for the first three quarters of the year.

![](images/barCharJobsFilledByYearQ1throughQ3.png)

So now that it's confirmed that hiring is down in 2020, it would be helpful to know where the missing positions who was been the most affected by the drop in hiring. 

## Salary

To gather some insight on what happened in 2020, let's start by taking a look at a box plot of salaries to get an idea of how well data scientists are paid.

![](images/boxPlotSalary.png)

So the first quartile has a salary of 83k, the median is 104k and the third quartile is 133k. Now let's break this down by year and see how salaries have been changing.

![](images/boxPlotSalaryByYear.png)

In summary, from 2015 to 2016, the salaries went down in every quartile. Then salaries went up and remained steady from 2017 to 2018. Then an increasing trend appears between 1 and 3 thousand dollars to the first quartile, median, and third quartile compared to the previous year. It's difficult to look at these plots and say that anything strange is going on, so let's take a look at how salaries have been changing from quarter to quarter.

![](images/boxPlotSalariesByYearAndQuarter.png)

There's a lot of information to sift through in this last plot, but I think the main focus should be that hiring in the first quarter is usually when the salaries are the lowest for the year. I would interpret this to mean that this is when the most early career employees are hired since they would be expected to have the lowest salaries. Notice that in 2020, the distribiution for salaries in the first quarter appears to be way up compared to previous first quarters. This could indicate that fewer early career positions were filled for the year. To make sure, let's take a closer look at the first quarters of each year.

![](images/boxPlotSalaryByYearAndQ1.png)

Now it should be clear that salaries are up in the first quarter. The first quartile, median, and third quartile are each up by about 10k. I would assume this means that fewer early career positions were created or filled due to uncertainty in how COVID-19 would affect the economy. We also know that hiring saw a huge increase in the second quarter compared to previous years, so it's possible that a lot of those early career positions were just filled later. To verify this, let's take a look at the salary distributions of the second quarter of each year:

![](images/boxPlotSalariesByYearAndQ2.png)

Here we can see that the second quarter made up for a lot of the missing early career positions that are usually filled in the first quarter. The first quartile, median, and third quartile positions are all down by about 13k, which should be an indicator that more early career positions were filled during this time. However, there were also fewer positions in total for the second quarter so it would be useful to see how the combined first and second quarter box plots have effected salary distributions.

![](images/boxPlotSalaryByQ1throughQ2.png)

With the two quarters combined we can see that the salary distribution for the combined first and second quarter in 2020 is still up compared to previous years by about 4k or more in the first quartile, median, and third quartile. This probably means that early careers positions were reduced in the first two quarters of the year. Remember, we only have the first three quarters of 2020 so the last comparison should be all data on the first three quarters of the year.

![](images/boxPlotSalaryByQ1ThroughQ3.png)

 We still see that the distribution for 2020 is up by about 4k in the first quartile, median, and third quartile compared to past years. So if the salaries are up, then why? Maybe the states and cities with the highest wages were hiring early career positions and that's why the salaries are seeing this boost. 

## Locations

Let's first take a look at the distribution of salaries by states. The states will be organized by median salary in descending order.

![](images/boxPlotSalaryByState.png)

![](images/barChartStateEmployment.png)

Now let's take a look at how the share of hiring by state has changed.

2015:
![](images/pieChartLocations2015.png)

2016:
![](images/pieChartLocations2016.png)

2017:
![](images/pieChartLocations2017.png)

2018:
![](images/pieChartLocations2018.png)

2019:
![](images/pieChartLocations2019.png)

2020:
![](images/pieChartLocations2020.png)

Note that California, New York, and Washington, have the highest salaries and the most data scientists, but their share of the data scientists hired each year has been steadily shrinking. In total, the percentage has gone from 71% of all positions in 2015 to 56% of all positions in 2020. So perhaps, the reason that salaries are up is because the biggest companies are hiring fewer early career positions than they used to.

## Big Companies

Let's start by exploring 

![](images/boxPlotSalaryByTop10Employer.png)

Note that all of these companies', except IBM, have median salaries that are considerably higher the median salary of data scientists as a whole. Now that we've seen what the distribution of these salaries look like, let's take a look at how these salaries have changed over time.

![](images/boxPlotSalaryByYearAndQ1ThroughQ3Top10Employers.png)

These box plots show that the top hiring data science companies have steadily been paying  raising the salaries of their newly hired employees each year. 2020 in particular saw the largest increase in the median salary of newly appointed data scientists at these companies with the first quartile, median, and third quartile all up by 10k compared to the previous year. Now let's take a look at how many positions were filled in the first three quarters of each year.

![](images/boxPlotSalaryByYearAndQ1ThroughQ3Top10Employers.png)

In this plot we can see that just like that just like the economy as a whole, the number of Data Science positions filled was increasing rapidly until we get to 2020 where there is only a slight increase. Now you might be wondering if the hiring patterns for the top 10 companies matches the hiring pattern of all employers.

![](images/barChartJobGrowthByYearAndQuarterTop10Employers.png)

As we can see the pattern matches what we saw earlier. Most positions were filled in the first quarter and this was also when salaries were at their lowest. Let's see if that pattern continues here too.

![](images/boxPlotSalaryByYearAndQuarterTop10Employers.png)

Just as before, the salaries the distribution of salaries is lowest during the first quarter of each year and then higher for each quarter afterwards. It also appears that the salaries have been steadily increasing. Let's investigate this further by comparing the salaries only in the first quarter. 

![](images/boxPlotSalaryByYearAndQ1Top10Employers.png) 

What's interesting to note here is that the first quartile and median salaries of positions in 2020 are up by 10k compared to 2019 but even 2019 saw 7k, 7k, and 15k, increases in the first quartile, median, and third quartile compared to 2018, respectively.

So maybe the largest companies that hire data scientists fill or create as many early career positions  as they had in previous years. If enough larger data science companies continued this pattern, then maybe this is the reason that salaries are up in 2020.  

## References

1. The data used for this analysis was scraped from h1bdata.info

2. The scraper used was cloned from this github repositoryhttps://github.com/mingen-pan/Scraping-H1B-visa-info by Mingen Pan.