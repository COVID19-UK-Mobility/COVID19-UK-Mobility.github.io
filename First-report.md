Authors:

**Clodomir Santana Jr.<sup>1</sup>, Federico Botta<sup>1</sup>, Hugo Barbosa<sup>1</sup>, Filippo Privitera<sup>2</sup>, Ronaldo Menezes<sup>1</sup>, Riccardo Di Clemente<sup>1</sup>**

<sup> 1 </sup> Department of Computer Science, University of Exeter
<br>
<sup> 2 </sup> Cuebiq Inc.

[Go back to home page](./index.html).
 
## Executive summary
 
 add here a brief summary of the first report
 
 

## Timeline of COVID-19 development in the UK
In January 2020, cases of the novel coronavirus started being reported outside of China. These cases were typically from people who had recently travelled to the Chinese Hubei province, where the disease started spreading. Events related to COVID-19 in the UK started unfolding at the end of January, with the first reported cases in the country. A brief timeline for the UK is the following:
   * <b>31st January 2020</b>: two Chinese nationals, one of whom studied at the University of York, were the first confirmed cases in the UK.
   * <b>6th February 2020</b>: a man in Brighton became the third confirmed case in the UK. He had previously travelled to Singapore and then visited a ski resort in France.
   * <b>10th February 2020</b>: the number of confirmed cases in the UK increases to 10, due to infections linked to the man in Brighton.
   * <b>27th February 2020</b>: the total number of confirmed cases is 16, with the first signs of infections spreading from the outbreak in Northern Italy due to people travelling back from the affected regions.
   * <b>1st March 2020</b>: the official number of cases is 36, and there are signs of infections amongst people with no history of recent travel abroad.
   * <b>11th March 2020</b>: the confirmed cases in the UK are now 456. The World Health Organisation declares the outbreak a pandemic.
   * <b>12th March 2020</b>: the UK Chief Medical Office raises the risk from moderate to high. Anyone with a new continuous cough or a fever is recommended to self-isolate for seven days, schools cancel trips abroad and people over 70 are asked to avoid cruises.
   * <b>13th March 2020</b>: many sporting events are postponed, as well as the 2020 UK local elections.
   * <b>16th March 2020</b>: the number of cases is over 1,500, and the number of deaths is 55. The Prime Minister advises against non essential travelling, and encourages people to avoid pubs, clubs and theatres. Working from home is encouraged.
   * <b>23rd March 2020</b>: the Prime Minister announces stricter measures for the UK coming into place from the following day (March 24th). People are asked to stay home except for essential food shopping, essential work travel and one form of exercise per day only with members of their household.
   * <b>26th March 2020</b>: the death toll is 422, and the number of people that tested positive is 11,568.
   * <b>27th March 2020</b>: both the Prime Minister and the Health Secretary announce testing positive for the virus.

Note that this timeline is not meant to be complete, but is only an indication of how major events related to COVID-19 unfolded in the UK over time, and which restrictions were put into place at what point in time. For a more complete report on the development of COVID-19 in the UK, you can <a href="https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_the_United_Kingdom" target = "_blank" rel = "no opener no referrer">read more here</a>. 

## The Analysis

### Baseline February 2020

In order to assess whether movement of people has reduced in the UK during the restriction measures, we first have to establish what the regular level of movement across country is. We refer to this as our baseline. We use the <em> radius of gyration </em> as our measure of mobility. The radius of gyration provides an indication of the characteristic distance travelled by a person during a given time period.
<br>
We estimate our baseline by considering the average mobility during the period xxx until yyy in February 2020. This period is immediately before restriction measures were put into place by the British government, and it does not contain significant events, such as bank holidays or festivities, that may affect our baseline estimates. For our baseline, we use the median radius of gyration. <b>Figure 1 (A)</b> depicts the results of our baseline estimates.
<br>
EDIT? As an example of a comparison between the baseline and another day, we selected the 25th of February and showed the comparison result in <b>Figure 1 (B)</b>. As can be noticed in this figure, in that day the radius increased or not changed in the majority of the regions of the Uk.

<br>
<figure class="image" align="center">
<img src="plots/uk_baseline.png" width="300">
<img src="plots/uk_reduc_25_02.png" width="300">
 <figcaption align="center"> <b>Figure 1</b> (A) We estimate the average levels of mobility across the UK to use as comparison throughout our analysis. As a measure of mobility, we use the radius of gyration, which indicates the typical distance travelled during the given time period. Here, we depict the median radius of gyration during the time period between xxx and yyy (note the logarithmic scale). Areas with more intense red correspond to areas with a larger value of the radius of gyration (B) We validate our baseline by comparing it to a typical day before the restriction measures came into place. Blue areas represent locations where the radius of gyration decreased, whereas grey areas represent no changes or an increase in the mobility. We find that, on a typical day, we do not observe many areas where the radius of gyration is lower than our baseline.</figcaption>
</figure>

### 12th March 2020

By March 12th 2020, the confirmed number of Covid-19 cases in the UK had increased to about five hundred  and the Chief Medical Officer advised schools to cancel school trips and recommended people with coronavirus symptoms (fever of dry continuous cough) to self isolate for seven days. <b>Figure 2</b> depicts the comparison between this day and the baseline. Visual inspection clearly reveals several areas which have a decreased radius of gyration, as compared to Figure 1 (B). However, the majority of locations still presents no decrease in the average mobility. 
<br>
<figure class="image" align="center">
<img src="plots/uk_reduc_12_03.png" width="350">
<figcaption align="center"> <b>Figure 2</b> We compare the average mobility on March 12th with our baseline estimates. We find that a number of locations present lower mobility, as measured by the radius of gyration. However, the majority of areas still have no decrease.</figcaption>
</figure>

### 23 March 2020

On March 23rd, the Prime Minister asks the British people to stop all non-essential travelling, effectively imposing a state of lockdown in the UK. We anticipate that this restriction measure will lead to a big reduction in the levels of mobility in the upcoming days. <b>Figure 3</b> presents the changes in the radius of gyration between this date and our baseline. We clearly see a reduction in the mobility of people across the majority of the UK.
<br>
<figure class="image" align="center">
<img src="plots/uk_reduc_23_03.png" width="350">
<figcaption align="center"> <b>Figure 3</b> Here, we present a comparison between the radius of gyration across the UK on 23rd March and the baseline mobility levels. We observe a reduction in the average mobility for most of the UK as a result of restriction measures put into place by the Government.</figcaption>
</figure>


### 01 April 2020

We anticipate that the restriction measures on people's mobility imposed by the British Government will take a few days to show their full effect. Here, we compare the median radius of gyration on April 1st with our baseline (<b> Figure 4</b>). We find a reduction in mobility across the majority of the United Kingdom.
<br>
<figure class="image" align="center">
<img src="plots/uk_reduc_01_04.png" width="350">
<figcaption align="center"> <b>Figure 4</b></figcaption>
</figure>


### The Trend of UK

<br>
<figure class="image" align="center">
<img src="plots/timeseries.png">
<figcaption align="center"> <b>Figure 5</b></figcaption>
</figure>


### Comparison Mobility Before and After Mobility Restrictions

Our goal is to assess whether restriction measures are having the desired effect in reducing the mobility of British people. Here, we directly compare the degree of mobility in different time periods across the four countries in the United Kingdom. After March 23rd, when an effective lockdown was imposed on the country, we see a great reduction in the levels of mobility across all of the UK.
<br>
<figure class="image" align="center">
<img src="plots/uk_geo_codes_before_after.png">
<figcaption align="center"> <b>Figure 6 UK</b></figcaption>
</figure>
<br>
<figure class="image" align="center">
<img src="plots/eng_detailed_regions_before_after.png">
<figcaption align="center"> <b>Figure 7 ENG</b></figcaption>
</figure>
<br>
<figure class="image" align="center">
<img src="plots/radious_weeks_nl.png" width="800">
<figcaption align="center"> <b>Figure 8</b></figcaption>
</figure>
<br>
<figure class="image" align="center">
<img src="plots/radious_weeks_sc.png" width="800">
<figcaption align="center"> <b>Figure 8</b></figcaption>
</figure>
<br>
<figure class="image" align="center">
<img src="plots/radious_weeks_wa.png" width="800">
<figcaption align="center"> <b>Figure 9</b></figcaption>
</figure>

### Validation of Data

Population plot the upper point of ENG are London
<figure class="image" align="center">
<img src="plots/pop_validation.png" width="800">
<figcaption align="center"> <b>Figure 9</b></figcaption>
</figure>

## Data

This research has been performed using data from anonymized users who have opted-in to provide access to their location data anonymously, through a GDPR-compliant framework. The single users were no identifiable at any research steps. The residential areas were inferred at an aggregated county level.

## Team

<a href="http://emps.exeter.ac.uk/computer-science/"> University of Exeter, Department of Computer Science: </a> team members from the Department of Computer Science have expertise in human mobility, data science, human behaviour and urban science.

<p>
<a href="https://www.cuebiq.com/"> Cuebiq Inc.</a> is a consumer insights company that analyzes visitation patterns based on aggregated and privacy-safe mobility data, to provide measurement, support academic research and humanitarian initiatives. 
</p>

## Contact us

If you have any questions, comments or would like to know more about our analysis, you can contact us at the following email addresses:
<br>
<a href = "mailto: r.di-clemente@exeter.ac.uk"> Riccardo Di Clemente</a>, Exeter University
<br>
<a href = "mailto: blake@cuebiq.com"> Brennan Lake</a>, Cuebiq Inc.

## Acknowledgments
This preliminary analysis is a collaboration between the Department of Computer Science of Universtiy of Exeter and Cuebiq Inc. In response to the COVID-19 crisis, <a href= "https://www.cuebiq.com/">Cuebiq</a> is providing insights to academic and humanitarian groups through a multi-stakeholder <a href="https://www.cuebiq.com/about/data-for-good/"> data collaborative</a> for timely and ethical analysis of aggregate human mobility patterns. We thank Pietro Gravino for the usefull discussions.

