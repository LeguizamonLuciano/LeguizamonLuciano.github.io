---
title: Power BI dashboard - bank marketing campaign
date: 2022-02-02 18:32:00 -0300
categories: [Projects, PowerBI]
tags: [transform, data]
pin: true
mermaid: true
---

> <a href="https://drive.google.com/file/d/1_l537mzgDz2mY6SNOULbAlLisRYnIVsh/view?usp=sharing">Documentation (spanish)</a>
{: .prompt-info }

## <u>About</u>

This dashboard was the final project for the data analytics course of the **Coderhouse** platform. The idea was to take a dataset of your choice and clean it to then organize it into different 5 tables that had to be related to each other (star scheme)

> The choice was not easy at all since I did not want to fall into a cliche (covid, gdp, environment, etc.)

After digging around kaggle for a few days I came across the following dataset which had true data, a good number of rows and many variables to analyze -> <a href="https://www.kaggle.com/volodymyrgavrysh/bank-marketing-campaigns-dataset">Bank mkt campaign dataset</a>

## <u>Topic</u>

The chosen dataset is related to direct marketing campaigns (phone calls) of a Portuguese banking institution

The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed

## <u>Features</u>

The dataset contains more than 20 attributes, more than 40K rows and the information is real. All the inputs are from May 2008 to November 2010

We can divide all attributes in 4 groups: 

1. bank client data (age, job, loans, etc)
2. related to last campaign (type of last contact, month of last contact, etc)
3. social and economic (inflation, bank loan interest, employee rate, etc)
4. other (contacts performed, days from last contact, etc)

 <div class="mermaid">
flowchart TB;
    subgraph Transforming data into insights
    Ask-->Prepare-->Process-->Analyze-->Share-->Act!
    end </div>

<div style="text-align:center;padding-bottom:21px"> <span style="color:green"><b><font size="5">Ask</font></b></span></div>

I was interested in knowing how effective the campaign was, that is, if the people it was addressed to were the right ones or if the bank had to adjust its parameters for future campaigns. From this arose the following and many other questions:

* What age range performed best?
* Does the income of money affect the result?
* Does the duration of the calls affect the result?
* Did the economic crisis of 2008 affect the performance if we compare it with other years?

<div style="text-align:center;padding-bottom:21px"> <span style="color:green"><b><font size="5">Prepare</font></b></span></div>

The dataset was analyzed in search of information that allows us to answer our questions, once identified, I segmented it and grouped it into several tables.

* Client data
* Contact client data
* Previous and current campaign
* Socioeconomic variables
* Calendar table 

Examples:

The "Client data" table had information exclusive to the client, such as age, type of job, marital status, education, balance and status of default with the bank.
The "Socioeconomic variables" table had information on inflation, bank interest, unemployment and consumer confidence

<div style="text-align:center;padding-bottom:21px"> <span style="color:green"><b><font size="5">Process</font></b></span></div>

To clean the data I mostly used PowerBI tools, Power Query Editor, table tools, columns and calculated measures

Null or empty values were removed, the date columns were adapted to the date table, the socioeconomic variables were normalized to refer exclusively to the period of the marketing campaign (thanks OECD)

I used calculated columns exclusively to group ages and duration of calls in 3 groups

<div style="text-align:center;padding-bottom:21px"> <span style="color:green"><b><font size="5">Analyze</font></b></span></div>

I consider this part the most important since it allows us to show, through graphics and different tools, the story we want to tell.

These graphs allowed us to understand much better what relationship exists between the data and to evaluate very quickly what affects the final result, such as the incidence of age or how the decrease or increase in bank interest affects the acquisition of a banking product.

For example with donut graphs I was able to quickly compare 8 variables in two different segmentations (current campaign and previous campaign)

![Desktop View](/dona.png)

<div style="text-align:center;padding-bottom:21px"> <span style="color:green"><b><font size="5">Final results</font></b></span></div>

> The duration of the call should exceed 5 minutes 
{: .prompt-tip }
> The best results are in those classified as single and students (best performance) 
{: .prompt-tip }
> Future marketing campaigns should not be carried out during periods of economic crisis or downturn in economic activity
{: .prompt-tip }

<div style="text-align:center;padding-bottom: 25px"> <u><b><font size="5">Dashboard details</font></b></u> </div>
The dashboard has a total of 13 pages, dark and light mode selector, segmentations, filters, bookmarks, page navigators, measures and many more things

- **The first 4 pages are:** front page, glossary and the navigation section (1 for dark mode and 1 for light mode). Each page has navigation bookmarks

- **The next 8 pages are:** actual campaign, last campaign, bank's clients and socioeconomic indexes 
(4 for light mode and 4 for dark mode + 1 segmentation for light mode + 1 segmentation for dark mode)

- **The last page** summarizes all the work showing relevant points and recommendations for the bank's managers

___

![Desktop View](/mainmain.png)
![Desktop View](/sndsnd.png)
![Desktop View](/last.png)