# Kickstarting Plays by Ben Altshuler

## Overview

Louise is crowdfunding a play on Kickstarter. In order to gain insight into group-funded creative projects, we delved deeply into a dataset consisting of thousands of campaigns.

### Purpose

Louise's fundraising team can use our information to grow or attenuate their goals, and plan their next kickstarter around the schedule we identified in the “Outcomes Based on Launch Date” section.

## Analysis and Challenges 
After whittling away some of the least relevant kickstarters in order to focus on similar sized play kickstarters, we were able to glean insight based on the time of the campaigns' introduction and their goals. Below are images of two charts plotted for Louise. One displays outcomes of play kickstarters based on the date of the kickstarter launch while the other shows outcomes based on the goal. 

### Analysis of Outcomes Based on Launch Date
Used pivot table to filter the sheet. Looking only at theater kickstarters, we filtered launch dates by years and months, in order to see what might separate successful crowd funds from failed ones. 

### Analysis of Outcomes Based on Goals
By stratifying our data across a spectrum of expected funds, we can see whether the amount sought influences the outcome of the campaign. We created rows of goal amounts, then used nested count-if statements to sort the different campaigns based on outcome. Here’s a sample formula from the sheet: “=COUNTIFS(Kickstarter!D:D,">=5000 ", Kickstarter!D:D, "<10000", Kickstarter!F:F, "=failed", Kickstarter!R:R, "plays" )”

### Challenges and Difficulties Encountered
The biggest difficulty was in applying the countif logic to multiple cells. There’s probably a more elegant solution, but I copied and pasted manually, changing the arguments to match up to the row. This is where I was missing something like a switch statement or a more algorithmic approach. There might be an Excel-y way to do this quickly, but I was slow and kept accidentally changing the formula of my copied cell when clicking into my targeted pasting cell. 

## Results

The clearest trend based on launch date is that Summer is the hot time to crowdfund plays. Out of 1369 play fundraisers, 457 launched in May, June, and July. A lot of these summer campaigns are successful, with almost twice as many succeeding as failing. This trend falls off as the weather cools; of 75 December campaigns, 35 failed and 3 were canceled. May seems to be the best time to launch a campaign, statistically. 

Looking at outcomes based on goals gets interesting. While our data is somewhat skewed towards smaller campaigns (186 projects sought less than 1000USD vs 16 wanting over 50,000), I feel comfortable claiming that there’s a negative correlation between goal and success. The most expensive campaigns seem generally the most likely to fail. This isn’t always true. All 4 campaigns in our set that sought between 30000 and 35000USD succeeded. Further research might reveal why these 4 succeeded with such lofty goals. ![Outcomes Based on Goals](Resources/Outcomes_vs_Goals.png?raw=true "Outcomes Based on Goals")

## Limitations
I think it might be helpful to know more about the backers than just how many each campaign had, surely kickstarter has a little more info on who’s using their site. Also, I think this kind of application has an element of creative marketing that is ignored here. This data set gives us no way to compare the actual Kickstarter pages’ CONTENT. We can see the blurb, but we all know a website is much more than the copy that comprises it. 

## Future Work
If we had more time for Louise, perhaps we could delve into average donation, and whether the average donation was influenced by goal or by genre or venue. Did any of our successful campaigns only succeed due to some mystery mega-backers? Were failed campaigns due not to the frequency of donations, but by small amounts? 
