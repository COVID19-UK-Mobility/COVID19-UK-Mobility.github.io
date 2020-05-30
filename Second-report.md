---

description: "Second report (13th May 2020): Analysis of socioeconomic aspects related to mobility patterns in the UK during the COVID-19 pandemic"

---

Authors:
**Clodomir Santana (1), Federico Botta (1), Hugo Barbosa (1), Filippo Privitera (2), Ronaldo Menezes (1) and Riccardo Di Clemente (1).**

(1) Department of Computer Science, University of Exeter.
<br>
(2) Cuebiq Inc.

[Go back to home page](./index.html).

<a href="reports/Covid19_Second_UK.pdf" download>Click here to download the report.</a>

### Disclaimer

<div style="text-align: justify">
These results/analyses do not necessarily reflect the views of the University of Exeter and it is not an official position of the University. The analyses here reflect the personal views of the aforementioned researchers. The reader should also be aware that, although we have used all tools necessary to ensure the correctness of our analyses, this work has not been independently peer-reviewed. We welcome your feedback on our analyses and methodology.
</div>

## Executive summary
<div style="text-align: justify">

Lockdown measures put in place around the world have affected people's lives at various levels. The debate about when they should start and end is endless, with many defending variations of it which consider age, health risk, the importance of labour for society (key workers), to name a few. In certain locations in the world, particularly in developing nations, the debate is between health issues (lockdown) vs. survivability (getting back to work); this debate is around health concerns and the economy and one that is hard to delve into. 

</div>

<div style="text-align: justify">

In line with the worries about the economy, a few world leaders have defended what is called <i>vertical</i> social isolation to "enable people in low income classes to earn a living" and "avoid further suffering from loss of income" [<a href="https://www.wsws.org/en/articles/2020/04/27/bols-a27.html">1</a>,<a href="https://riotimesonline.com/brazil-news/brazil/bolsonaro-to-call-on-mandetta-to-isolate-only-the-elderly-and-sick/">2</a>,<a href="https://eu.freep.com/story/news/local/michigan/2020/05/21/donald-trump-ford-motor-restart-american-economy/5239965002/">3</a>]. Although these policies have not been in place in the UK we explore what has been the <i>de facto</i> effect of lockdown policies to different social classes in several regions of the UK.
</div>

### Summary of main findings

<div style="text-align: justify">

In this report, we show that low-income groups have never attained the same level of restrictions as high-income groups in the UK. This means that social isolation policies disproportionally affect different groups, with high-income groups being the most able to restrict their movement. We focused the analysis on four periods depicted in <b>Figure 2</b>, henceforth called P1 (from 11/3/2020 to 23/3/2020), P2 (from 23/3/2020 to 5/4/2020), and P3 (from 5/4/2020 to 17/4/2020). We kept the length of the periods roughly the same to ensure fairness in the analysis. We use these 3 periods to contrast the level of movement restriction for different social classes in a period before the announcement of the UK partial lockdown (P1), the period after the announcement until movement levels started to stabilise around the date of the historic TV broadcast from Queen Elizabeth II (P2), and the period after the broadcast until 17 of April (P3). We show that P3 shows an increase in the levels of mobility for lower classes which may be a sign of people getting tired of lockdown restrictions, venturing outside their homes, or even being required to work to provide for their families. The increase in mobility in P3 varies significantly around the UK. Lastly, we show that normal rhythms of individuals which arise from our daily routines are completely lost after the suggestion that people should "avoid crowded places and work from home if possible" (17/3/2020); this means that such measures lead to people having variety in their rhythms or even not having regular rhythms.

<br>
<figure class="image" align="center">
<img src="plots/second-report/mobility_activity.gif"  width="600"/>
<figcaption align="center"> <b>Figure 1</b> <div style="text-align: justify"><i>Evolution of the mobility activity in the UK, ENG, NIR, SCT and WAL since the announcement of the partial lockdown in 23rd of March.</i>
</div></figcaption>
</figure>
<br>

</div>

### General Information and Methods

As indicated earlier, this report focuses on variations in human mobility as a function of socioeconomic status but also looking at specific periods in the last two months of the pandemic. **Figure 2** gives us a general overview of mobility patterns for the entire UK. This general view demonstrates a clear change in patterns which we explored in our <a href="https://github.com/COVID19-UK-Mobility/COVID19-UK-Mobility.github.io/blob/master/First-report.md">First Report</a>. Yet, this figure also shows us a stabilisation in the mobility restrictions and perhaps even a slight increase in P3. However, the figure does _not_ show how each different socio-economic groups compare to these general patterns, that is, do lockdown restrictions affect (or are implemented by) socio-economics groups differently?

<br>
<figure class="image" align="center">
<img src="plots/second-report/uk_trends_periods.png"  width="600"/>
<figcaption align="center"> <b>Figure 2</b> <div style="text-align: justify"><i>Updated evolution of the mobility activity over time for the UK compared to the baseline (average mobility between 1st and 4th February 2020). We divided the series into 3 periods: the first one (P1) is highlighted in blue and goes from 11 of March until the day where the partial lockdown was announced in the UK (23rd March). The second period (P2), represented in yellow, starts when the partial lockdown was announced and finished when the mobility activity levels begin to stabilize (5th of April). The penultimate period (green region of the plot) is defined between 5th and 17th of April. In P3, we noticed an increase in mobility activity in some regions of the UK. Finally, the last period (P4) represented by the colour red confirms the increase the mobility activity from 10 to 22 of May 2020. The important dates here are roughly the same ones used in Figure 5 in <a href="https://github.com/COVID19-UK-Mobility/COVID19-UK-Mobility.github.io/blob/master/First-report.md">First Report</a>. However, here we wanted to ensure the lengths of P1, P2, P3 and P4 are the same.</i></div></figcaption>
</figure>

<br>

Coupled with **Figure 2**, we can see in **Figure 3** that we indeed have an increase in mobility levels in the UK from P2 to P3 but also individually in all countries within the UK except for Northern Ireland. It also shows an increase in the degree of mobility in the UK and all of its four countries in the fourth period.

<br>
<figure class="image" align="center">
<img src="plots/second-report/uk_geo_codes_before_after_part_1.png"  width="400"/>
<figcaption align="center"> <b>Figure 3</b> <div style="text-align: justify"><i>Comparison between the mobility levels on the end of the fist (23th of March), second (5th of April), third (17 of April) and fourth (22 of May) periods in the UK, England, Nothern Ireland, Scotland and Wales. As observed, in most of the regions there was an increase in the mobility activity in P3 and P4.</i>
</div></figcaption>
</figure>


<br>
We used an analysis based on the speed at which mobility patterns have changed by looking at individual locations (at the local authority level) at the beginning and end of each period and calculating the slope of the line segment that links the two positions. **Figure 4** shows how this is done. In summary, the larger the degree of change in mobility, the steeper the line segment. We have 3 basic cases shown in **Figures 4(A), 3(B) and 3(C)** representing an increase of mobility levels, no change, and a decrease, respectively. After doing this, each location has a slope associated with it for each of the four periods.

<br>

<figure class="image" align="center">
<img src="plots/second-report/slope_ex.png"  width="600"/>
<figcaption align="center"> <b>Figure 4</b> <div style="text-align: justify"><i>To estimate the direction and magnitude of the levels of degree of mobility in a period, the following approach was adopted: for each period, we used a linear regression model to find a line which connects the point that represents the degree of mobility at the start of the period to the point at the end of the period. The magnitude of the slope of this line will indicate how big was the difference while the sign tells if it was a reduction (negative) or an increase (positive) in the mobility levels. Figure 2(A) shows a scenario of increasing mobility (slope > 0) and Figure 2(C) depicts the opposite case (slope < 0). A slope value close to zero, Figure 2(B), indicates a small difference in the degree of mobility between the points considered.</i>
</div></figcaption>
</figure>
<br>

### First Period: from 11 to 23 of March 2020

This is the period during which people in the UK were being told to stay at home and avoid all but essential trips. **Figure 5(A)** looks at local authorities with high density (density greater or equal to 1033.0 inhab/km²) versus low density (less than 1033.0 inhab/km²); the figure indicates that the <i>stay at home</i> message had a different effect in high and low-density local authorities. Locations with high density tend to have a small degree of mobility but from these,  local authorities with a higher degree of mobility had a higher degree of change (slope). For the case of low density areas, we see a milder effect and a wider diversity of degree of mobility; even at the end of the period some locations still have a high degree of mobility despite the significant decreases (slope).

**Figure 5(B)** looks at the changes in mobility based on the total annual household income in 2018 in each of the local authorities. The locations were divided into two groups: one with the local authorities with annual household income less than £43,500 (low-income group) and another composed of local authorities with an annual household income greater or equal to £43,500 (high-income group).  During this first period, we see that both low and high-income groups reduced their mobility and as expected the reduction happened at all levels of mobility from areas with low mobility to areas with high mobility. However, it is striking that this figure shows that for consistently low-income local authorities did not reduce their mobility at the same level as similar areas of high income.
<br>

<figure class="image" align="center">
<img src="plots/second-report/slope_radius_p1.png" width="600"/>
<figcaption align="center"> <b>Figure 5</b> <div style="text-align: justify"><i>Analysis of the impact that population density (A) and annual income (B) of local authorities in the UK have on the slope of the line and the degree of mobility at the end of the period. The groups represented by the green and yellow colours were obtained with the division of the data into two equal-sized groups based on sample quantiles. The lines are the output of linear regression for its respective group (colour). These plots show that the reduction in mobility was greater in areas with low density and the ones with high income.</i>
</div></figcaption>
</figure>
<br>

With the results depicted in **Figure 6**, we wanted to have a better understanding of how important the population density and the annual income are to the results presented in **Figure 5**. **Figure 6(A)** looks at how the annual household income and the population density are associated with the final degree of mobility in each local authority. As can be seen in **Figure 6(A)**, the variation in the final degree of mobility is more related to the population density than to the income.  This might be to the fact that in a low-density area, such as rural areas, people tend to have a longer trajectory to work/study when compared to a high-density area such as cities.

**Figure 6(B)** shows looks at how the annual household income and the population density are associated with the slope (how large was the reduction in the mobility). As observed in **Figure 6(B)**, both the annual household income and the population density of the local authorities influence the slope of the line. Also, the plot shows that the greatest slopes were generally related to areas with high income and high density.

<br>

<figure class="image" align="center">
<img src="plots/second-report/density_income_p1.png"  width="600"/>
<figcaption align="center"> <b>Figure 6</b> <div style="text-align: justify"><i>In this analysis, we wanted to have a better understanding of how important the population density and the annual income are to the results achieved in terms of the slope and the final degree of mobility. The contours represent the bivariate kernel estimate of the data and both axes are in a logarithm scale for better visualisation.</i>
</div></figcaption>
</figure>
<br>

### Second Period: from 23 of March to 05 of April 2020

The second period of our analysis contains the peak of the lockdown and probably the time in which the government invested the most in convincing the population to stay at home. There were numerous campaigns from all walks of society to incentivise people to _stay safe_ and _protect the NHS_ by _staying at home_. This was the period in which we also had the television address by Queen Elizabeth II. In this period, depicted in **Figure 7(A)**, we see high-density areas not reducing their degree of mobility much. This is probably due to the fact that their degree of mobility was already small. Conversely, the low-density areas have a more diverse set of change in mobility diversity. The income analyses continue to show a decrease in mobility but again high-income regions consistently have a stronger decrease in mobility.

<br>
<figure class="image" align="center">
<img src="plots/second-report/slope_radius_p2.png" width="600"/>
<figcaption align="center"> <b>Figure 7</b> <div style="text-align: justify"><i>In the second period assessed, we observed similar results to the previous period where we can see a reduction in the degree of mobility in both groups of income and population density; however, it is worth mentioning that, when compared to the first period, the slope and the final degree od mobility are smaller.</i>
</div></figcaption>
</figure>
<br>

Similarly to the previous period, we can see in **Figure 8(A)** that the final degree of mobility is greater in the local authorities with low population density and we see that there is no clear relationship between the annual population income and the final degree of mobility. Moreover, as shown in **Figure 6(B)**, **Figure 8(B)**  indicates that both the income and population density are associated the slope of the line. It worth mentioning that, compared to the previous period, the values of slope and final mobility are smaller.

<br>

<br>
<figure class="image" align="center">
<img src="plots/second-report/density_income_p2.png"  width="600"/>
<figcaption align="center"> <b>Figure 8</b> <div style="text-align: justify"><i>The results depicted in this figure were similar to the ones in Figure 6 where the final degree of mobility is more related to the population density of the local authorities and both the density and the annual income of the household influence the slope of the curve.</i>
</div></figcaption>
</figure>
<br>

### Third Period: from 05 to 17 of April 2020

The penultimate period of our analyses supports the claim that different regions and income levels are affected by lockdown measures differently. For the regions with high and low density, we do not see much of a difference and most of them have maintained their mobility levels (slope is around 0). However, for income, we observe that the low-income areas appear to slowly be increasing their mobility levels. When looking at **Figure 9(B)** it is clear that low-income regions tend to be above the slope 0 while high income tends to be below. This supports the idea that although not implemented in the UK, vertical isolation appears to be in fact in place. Low-income regions never stayed in isolation at the same levels seen by high-income areas, and more recently they have slowly increased their mobility while high-income areas continue to decrease their mobility levels (even if by a small margin).

<br>
<figure class="image" align="center">
<img src="plots/second-report/slope_radius_p3.png" width="600"/>
<figcaption align="center"> <b>Figure 9</b> <div style="text-align: justify"><i>Here we start to see the appearance of local authorities which have a positive slope of their line indicating an increase in the mobility degree in this period. Notice that this behaviour was observed in the income and population density groups.</i>
</div></figcaption>
</figure>
<br>

Furthermore, **Figure 10(A)** reviews that at the end of the second period the local authorities with low population density present the largest degree of mobility. **Figure 10(B)**  shows that there were areas with a small increase or decrease in the mobility degree in local authorities with low and high income/density.

<br>

<figure class="image" align="center">
<img src="plots/second-report/density_income_p3.png"  width="600"/>
<figcaption align="center"> <b>Figure 10</b> <div style="text-align: justify"><i>The colour patterns in this figure are also different from the one depicted in Figure 6 and Figure 8. We can no longer see a clear relationship between income/density and the results in terms of slope and final degree of mobility.</i>
</div></figcaption>
</figure>
<br>


### Fourth Period: from 10 to 22 of May 2020

The last period of our analyses shows that there is a trend of increasing the degree of mobility in the local authorities. **Figure 11(A)** shows that the largest increases were registered in local authorities with low density; however, the slope of the line indicates a similarity between the increase rate of low and high-density areas. Concerning the relationship of the slope and final degree of mobility with the annual household income, **Figure 11(B)** that the result for the low-income group was more concentrated in the area of the plot where the final degree of mobility was less than 4 and the slope less than 2.  On the other hand, the high-income local authorities were more distributed along the regression line.  In fact, **Figure 12(A)** also indicates that local authorities with high population density present, in general,  a smaller final degree of mobility.  **Figure 12(B)** shows that the slope of the line depends on both the annual household income and the population density of the local authorities.

<br>
<figure class="image" align="center">
<img src="plots/second-report/slope_radius_p4.png" width="600"/>
<figcaption align="center"> <b>Figure 11</b> <div style="text-align: justify"><i>The plots show a general increase in the mobility level among the local authorities in the UK. Although we can see an increase in almost all local authorities regardless of the population density and annual household income, we can observe that the increase was greater in some of the low-density and high-income areas.</i>
</div></figcaption>
</figure>
<br>


<br>
<figure class="image" align="center">
<img src="plots/second-report/density_income_p4.png"  width="600"/>
<figcaption align="center"> <b>Figure 12</b> <div style="text-align: justify"><i>The patterns depicted in these figures indicates that the relationship between the population density with the final degree of mobility is stronger than the relationship between annual household income and the final degree of mobility. On the other hand, both the population density and the annual household income influences the slope of the regression line.</i>
</div></figcaption>
</figure>
<br>

An increase in the degree of mobility during the lockdown were also observed in the US, where the mobility activity of the population began to increase even though the mobility-restriction measures were not lifted [<a href="http://news.northeastern.edu/2020/05/26/people-in-the-us-started-moving-around-more-before-stay-at-home-measures-were-lifted">4</a>]. These results are also supported by articles which report an increase in the number of people at beaches and parks in the UK [<a href="https://www.mirror.co.uk/news/uk-news/uk-abandoned-social-distancing-photos-22087839">5</a>].

<br>

### Mobility Synchronisation

In addition to the mobility levels, the mobility _synchronisation_ (i.e., how many people are leaving their homes at the same time) is another important facet of the human travelling behaviour of relevance for the covid-19 prevention efforts. Indeed, human mobility patterns are known to exhibit a large degree of temporal regularities, especially when it comes to commuting behaviours. These regularities are mostly governed by the synchronisation of labour, our work schedules and the activities we accomodate around them. 



In the context of the covid-19 outbreak analyses, the mobility levels and travel _distances_ are important estimates of _how much_ people are traveling, while the mobility synchronisation metric would affect how much _exposure_ those trips could potentially produce.  Thus, we computed for each areal unit how many people where leaving _home_ every hour. In **Figure 13** we compare the out-of-home trips for the first week of February in 2019 and the first week of April in 2020. It is clear that the lockdown measures imposed in the UK were effective in reducing the number of out-of-home trips.

<br>
<figure class="image" align="center">
<img src="plots/second-report/out_of_home_trips1.png"  width="600"/>
<figcaption align="center"> <b>Figure 13</b> <div style="text-align: justify"><i>Here we use the first week of February 2019 as a baseline for what would be a standard behaviour in terms of the number of out-of-home trips. For the reference week, it is evident that the mobility  exhibit a large degree of temporal regularity with two daily peaks (morning and evening) with this pattern repeating every weekday. When we look at the first week of April 2020 it is evident that lockdown measures imposed in late-March were very effective in restricting the out-of-home trips in the UK.</i>
</div></figcaption>
</figure>
<br>


From **Figure 13** it is easy to spot the presence of marked temporal regularities indicating that people tend to leave home at regular time intervals indicating that a large proportion of the out-of-home trips tend to happen in a synchronised fashion. Under normal circumstances, this phenomenon can be easily observed, for instance, in the high volume of cars and public transport passengers around certain hours of the day (e.g., rush hours).


However, such mobility synchronisation is not limited to conventional commuting times. In fact, it can happen at any time of the day in which people tend to perform certain activities. It can range from segments of the population with different working patterns (e.g., school teachers, healthcare professionals, hospitality workers ) to certain times of one's routine reserved for specific activities (e.g., eating, exercising, socialising).


Thus, in order for us to have a more precise picture of the mobility synchronisation patterns, instead of analysing it as a concentration of trips around certain hours, we define the _mobility synchronicity_  as the total magnitude in the _periodicity_ in the out-of-home trips. We, therefore, analysed the Wavelet and Fourier spectra to determine the strongest frequency components in the mobility regularity from our reference week from February 2019. Our analysis indicated that the mobility patterns are characterised by four main periods, namely 24h, 12h and 8h as seen in **Figure 14**.

<br>
<figure class="image" align="center">
<img src="plots/second-report/global_power.png"  width="600"/>
<figcaption align="center"> <b>Figure 14</b> <div style="text-align: justify"><i>Global Wavelet and Fourier for the out-of-home trips spectra indicating the presence of four main periods above the 95% confidence level: 24h, 12h and 8h</i>
  </div></figcaption>
</figure>
<br>

Next, we defined a mobility synchronicity metric as the sum of the  powers from the Lomb-Scargle periodograms corresponding to the 24h, 12h and 8h.  Following, we computed the mobility synchronicity  for the out-of-home trips in each week in our data (weeks 6 to 17). A higher synchronicity value for a given week means that more people left their homes at the same time in that week, potentially increasing the likelihood being exposed to the virus or exposing more people.



Our analyses indicated that before the partial lockdown measures, the overall out-of-home trips exhibited a large level of synchronicity, suggesting that the activity schedules were still in place. However, the partial lockdown measures put in place on 20 March significantly impacted the mobility synchronicity. Without the necessity to commute to work in face of the country-wide closure of non-essential activities, the out-of-home trips were more scattered throughout the day, reducing the likelihood of agglomerations and therefore the spread of the disease. 


<br>
<figure class="image" align="center">
<img src="plots/second-report/mobility_sync.png"  width="600"/>
<figcaption align="center"> <b>Figure 15</b> <div style="text-align: justify"><i>The synchronicity metric reveals that in general, the out-of-home trips were less synchronised than the reference 2019 reference week. Furthermore, it shows that the partial lockdown measure imposed on 20th March was effecting also in reducing the mobility synchronisation, descreasing therefore the likelihood of contagion. It also appears that in the last week of the analysis we see an uptick on the synchronicity levels which is in line with what we demonstrated earlier for P3.</i>
  </div></figcaption>
</figure>
<br>

#### Regional Differences in Mobility Synchronisation

Here we compared how the partial lockdown measures put in place in 20th March affected the out-of-home mobility synchronicity across the different regions of England. It is clear that, for all regions, the lockdown reduced the synchronisation of the mobility behaviour. However, some regions still sustained a reasonable degree of synchronicity (e.g., East of England and the South West) whereas for other regions such as Yorkshire and The Humber there was a significant reduction in the mobility synchronisation. 

<br>
<figure class="table" align="center">
    <figcaption align="center"> <b>Table 1 - Mobility synchronisation for the different regions of England. </b> <div style="text-align: justify">
  </div></figcaption>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: center;">
      <th>Region</th>
      <th>Pre-lockdown</th>
      <th>During lockdown</th>
      <th>Reduction</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Yorkshire and The Humber</td>
      <td>0.71</td>
      <td>0.30</td>
      <td>0.41</td>
    </tr>
    <tr>
      <td>East Midlands</td>
      <td>0.79</td>
      <td>0.40</td>
      <td>0.39</td>
    </tr>
    <tr>
      <td>West Midlands</td>
      <td>0.77</td>
      <td>0.44</td>
      <td>0.34</td>
    </tr>
    <tr>
      <td>London</td>
      <td>0.83</td>
      <td>0.56</td>
      <td>0.27</td>
    </tr>
    <tr>
      <td>North East</td>
      <td>0.64</td>
      <td>0.40</td>
      <td>0.24</td>
    </tr>
    <tr>
      <td>South East</td>
      <td>0.81</td>
      <td>0.60</td>
      <td>0.21</td>
    </tr>
    <tr>
      <td>North West</td>
      <td>0.81</td>
      <td>0.62</td>
      <td>0.18</td>
    </tr>
    <tr>
      <td>South West</td>
      <td>0.72</td>
      <td>0.56</td>
      <td>0.16</td>
    </tr>
    <tr>
      <td>East of England</td>
      <td>0.61</td>
      <td>0.49</td>
      <td>0.12</td>
    </tr>
  </tbody>
</table>
</figure>
<br>

#### Socioeconomic Differences in Mobility Synchronisation

In addition to the regional differences, we also investigated how the mobility restriction measures and the partial lockdown affected the mobility patterns of populations from different socioeconomic groups according to the Office of National Statistics Socio-economic Classification (SEC). However, our highly-anonymised mobility data does not contain any socioeconomic metadata associated with the users. To overcome such limitation, we estimated the contribution of the population from the different socioeconomic  groups to the out-of-home trips by computing the average number of trips weighted by the populations of each of the eight Socioeconomic Classes, which can be described as follows:

<br>

| SEC   |  Description                                            |
| ---- | ------------------------------------------------------------ |
| 1    | Higher managerial, administrative and professional occupations |
| 2    | Lower managerial, administrative and professional occupations |
| 3    | Intermediate occupations                                     |
| 4    | Small employers and own account workers                      |
| 5    | Lower supervisory and technical occupations                  |
| 6    | Semi-routine occupations                                     |
| 7    | Routine occupations                                          |
| 8    | Never worked and long-term unemployed                        |

<br>
Our approach was to use a strategy that would not incorporate any differences in the mobility patterns at the socioeconomic level. Thus, in our weighted-average approach, we assumed that the total number of out-of-home trips within each Local Authority was uniformly distributed across each of SEC groups. The differences, therefore, would only be visible at a large-scale level when the populations and the corresponding contributions from the different SECs were aggregated over the hundreds of areal units.



**Figure 16** indicates that higher income populations (SEC 1 and SEC 2 ) were the ones with the smallest degree of mobility synchronisation. It could suggest that people in these positions  were already less synchronised due to less rigid working patterns. For the lower income groups, on the other hand, their synchronisation levels were always very close to the baseline.  It was only  after the lockdown measures of 20th of March that they became less synchronised. Still, comparatively speaking, lower SECs exhibited a larger degree of out-of-home mobility synchronisation than populations from other groups. Also, the lower the SECs the bigger the increase in synchronicity in the last few weeks of our analyses which reinforces the argument of inequalities leading lower SECs population to a "forced" return to a regular work pattern.

<br>
<figure class="image" align="center">
<img src="plots/second-report/socioeconomic_sync2.png"  width="600"/>
  <figcaption align="center"> <b>Figure 16</b> <i>Mobility synchronisation across different socioeconomic groups</i> <div style="text-align: justify">
  </div></figcaption>
</figure>
<br>

### Updated Mobility Trends in England

These charts are updated trends presented in the <a href="https://github.com/COVID19-UK-Mobility/COVID19-UK-Mobility.github.io/blob/master/First-report.md">First Report</a>.

<br>
<figure class="image" align="center">
<iframe src='https://flo.uri.sh/visualisation/2628094/embed' frameborder='0' scrolling='no' style='width:100%;height:800px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/2628094/?utm_source=embed&utm_campaign=visualisation/2628094' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>
</figure>
<br>

### Updated mobility trend in Northern Ireland

<br>
<figure class="image" align="center">
<iframe src='https://flo.uri.sh/visualisation/2629318/embed' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/2629318/?utm_source=embed&utm_campaign=visualisation/2629318' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>
</figure>
<br>

### Updated mobility trend in Scotland

<br>
<figure class="image" align="center">
<iframe src='https://flo.uri.sh/visualisation/2629340/embed' frameborder='0' scrolling='no' style='width:100%;height:800px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/2629340/?utm_source=embed&utm_campaign=visualisation/2629340' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>
</figure>
<br>

### Updated mobility trend in Wales

<br>
<figure class="image" align="center">
<iframe src='https://flo.uri.sh/visualisation/2629377/embed' frameborder='0' scrolling='no' style='width:100%;height:700px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'><a class='flourish-credit' href='https://public.flourish.studio/visualisation/2629377/?utm_source=embed&utm_campaign=visualisation/2629377' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;'> </a></div>
</figure>
<br>


## Data & Methods
<div style="text-align: justify">
This research has been performed using data from anonymized users who have opted-in to provide access to their location data anonymously, through a GDPR-compliant framework. The single users were not identifiable at any research steps. The residential areas were inferred at an aggregated local authority level. The analysis has been performed on a sample 250K users across the UK. We performed the radius of gyration analysis using the definition of (<a href="https://doi.org/10.1038/nature06958">Gonzalez, M. et al Nature 2008</a>). Moreover, each mobility value of a given region is the median value of the distribution of the radius of gyration of the users within a temporal window of 8 days centred around a given day.</div>

## Team
<div style="text-align: justify">
<a href="http://emps.exeter.ac.uk/computer-science/"> University of Exeter, Department of Computer Science: </a> team members from the Department of Computer Science have expertise in human mobility, data science, human behaviour and urban science (see disclaimer above).</div>

<p>
<div style="text-align: justify">
<a href="https://www.cuebiq.com/"> Cuebiq Inc.</a> is a consumer insights company that analyzes visitation patterns based on aggregated and privacy-enhanced mobility data, to provide measurement, support academic research and humanitarian initiatives.</div>
</p>

## Contact us
<div style="text-align: justify">
If you have any questions, comments or would like to know more about our analysis, you can contact us at the following email addresses:
<br>
<a href = "mailto: r.di-clemente@exeter.ac.uk"> Riccardo Di Clemente</a>, Exeter University
<br>
<a href = "mailto: blake@cuebiq.com"> Brennan Lake</a>, Cuebiq Inc.
</div>
## Acknowledgments
<div style="text-align: justify">
This preliminary analysis is a collaboration between the Department of Computer Science of University of Exeter and Cuebiq Inc. In response to the COVID-19 crisis, <a href= "https://www.cuebiq.com/">Cuebiq</a> is providing insights to academic and humanitarian groups through a multi-stakeholder <a href="https://www.cuebiq.com/about/data-for-good/"> data collaborative</a> for timely and ethical analysis of aggregate human mobility patterns. We thank Pietro Gravino for the useful discussions.</div>
<br>

<div style="text-align: justify">
When citing the content of this report, please cite as:
Clodomir Santana, Federico Botta, Hugo Barbosa, Filippo Privitera, Ronaldo Menezes, and Riccardo Di Clemenete (2020), Analysis of socioeconomic aspects related to mobility patterns in the UK during the COVID-19 pandemic, https://covid19-uk-mobility.github.io/Second-report


