# Understanding Summer Trends More and DIN/Chlorophyll Investigation

### Goals From Last Meeting:
1. Work on integrating new KC data + Ecology historical into LO - README + Parker review.
2. Follow up with Metro Vancouver.
3. Contact Christopher Krembs (Ecology) for data discussion.
4. Homeworks!
5. Further investigate trends using different statistical methods (e.g., varying summer seasons, trend tests, bootstrapping).
6. Continue to investigate correlations with Skagit flow and other environmental variables (ref. Banas MacCready Long Live the Kings report).
7. Write write write.
8. Start thinking about Parker's website update on trends.
   
### Completed Goals:
1. More work with understanding summer definition impact on trends - new plots.
2. Time series analysis of NO3/Chl - not enough data!


---

## Improving Summer Trends Visualization

Last meeting, we had a good conversation about the communication of "near-0" trends in plots. We decided to no longer use the 95% confidence interval accept/reject null hypothesis using a Mann-Kendall test for monotonocity, and instead just plot the 95% confidence intervals for each slope in each location.

NOTE: I'm using Thiel-Sen slopes and the "maximum" 95% confidence interval from that analysis. Thiel-Sen slopes use medians, and so the 95% confidence interval maximum and minimum slopes are not necessarily symmetric. However, in this case I've taken the absolute value of the high and low slope deviations from the Thiel-Sen slope. This gives a conservative, symmetric range that was easy to compare to previous linear regression confidence intervals. I'm happy to discuss this use more.

Here's the plots for all casts using Thiel-Sen slopes with 95% confidence for all measured variables. First, I've colored varying summer definitions separately. Large dots are the reported Thiel-Sen slope and the small dots are the higher and lower 95% confidence interval slopes.

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/20310355-c7b4-40de-bb24-1494771623cf" width="800"/><br>Fig 1. Surface DO trend slopes [mg/L/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/e0ff4bcc-e31c-4862-90cf-b2e4b98f122e" width="800"/><br>Fig 2. Deep DO trend slopes [mg/L/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/2809700d-bb53-4faa-b863-2fa3176e6123" width="800"/><br>Fig 3. Surface CT trend slopes [deg C/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/852f00d0-a6fa-4ba2-8671-ffc83251df51" width="800"/><br>Fig 4. Deep CT trend slopes [deg C/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/5212e00d-9b8d-4a48-89f5-7e3608c31086" width="800"/><br>Fig 5. Surface SA trend slopes [psu/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/9b62639f-4961-443f-bb29-a9e0d3358c00" width="800"/><br>Fig 6. Deep SA trend slopes [psu/century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/10a30d56-3e68-4996-bcec-01579df1ed61" width="800"/><br>Fig 7. Stratification trend slopes [sigma diff./century] at various sites, under various summer defintions.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/03a06a97-5ceb-4bc4-ae70-ea122589caf1" width="800"/><br>Fig 8. Surface DO saturation trend slopes [mg/L/century] at various sites, under various summer defintions.</p><br>

Statistically, if a 95% confidence interval encompasses the 0-slope line, then that particular slope would be considered statistically no-different than 0.

As usual, the strongest trends we observed are warming. Nearly all summer definitions and at all locations, we observe surface and deep warming. However, most seasons show very little difference from the 0-slope for surface and deep DO, with the exception of Near Seattle Offshore deep DO, which shows a decrease, and Saratoga Pasage Mid surface DO, which shows an increase.

A big takeaway I'd like to get from this meeting is **how to deal with variation caused by different summer definitions**. We've previously discussed "averaging" all of these slopes, but I find that the definitions I've selected for summer are somewhat arbitrary anyway and I'm having a hard time justifying their selection. I'm somewhat inclined to choose the August-November metric because that seems to capture most of the late-summer DO minima. But I'd love input here.

Looking at just the August-November "summer" definition:

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/0cb788dc-02f3-44da-b320-eabd7b4328a9" width="800"/><br>Fig 9. Surface DO trend slopes [mg/L/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/f46c671c-8f57-4abd-be2d-e6cdfb3ad715" width="800"/><br>Fig 10. Deep DO trend slopes [mg/L/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/6ccae012-15b7-489f-a4e8-64edf8a69b72" width="800"/><br>Fig 11. Surface CT trend slopes [deg C/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/e982242c-5238-4924-a318-ff50399a4044" width="800"/><br>Fig 12. Deep CT trend slopes [deg C/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/41e6f7d3-ac92-4cf2-afef-018e8791c81a" width="800"/><br>Fig 13. Surface SA trend slopes [psu/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/89162847-d046-48cb-b9d1-55aa0b283a85" width="800"/><br>Fig 14. Deep SA trend slopes [psu/century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/65936781-121b-4508-b084-182adaf96f38" width="800"/><br>Fig 15. Stratification trend slopes [sigma diff./century] at various sites from August-November.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/68018796-6f6c-4dea-af4f-c2c406938917" width="800"/><br>Fig 16. Surface DO saturation trend slopes [mg/L/century] at various sites from August-November.</p><br>

Some issues with using this summer definition may be that it does sometimes capture the winter storm start, which in Lynch Cove looks like it may have a singificant impact on the variation in the slopes for surface salinity? This is vexing me!!!

---

## DIN and Chlorophyll Trend Analysis Attempt

From last week, we also discussed finally performing the same trend analysis at my long time-history sites. I assessed NO3, chlorophyll, NO2, and NH4. NO2 and NH4 had nearly no time record at all time histories. NO3 and chlorophyll had enough data for a trend analysis, but do not meet the criteria for a 60-year time history at each site (they don't have the same length of record for DO/SA/CT and NO3/Chl). Here's the time series plots, but in my opinion any calculated trends are not particularly useful given the spotty time record and the extreme resolution differences before and after the late 90s. NOTE: I'm using yeardays 125-325 to bound these data points (summer definition: ~85% of hypoxic days).

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/3984f3d8-da5b-4ba3-ae24-9554cafc24a5" width="800"/><br>Fig 17. Summer surface and deep NO3 at Point Jefferson.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/b0a41739-eb1f-48f9-b640-6a7ecb42d6d7" width="800"/><br>Fig 18. Summer surface and deep chlorophyll at Point Jefferson.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/596b1a41-ef5d-4192-941d-526e9a83deae" width="800"/><br>Fig 19. Summer surface and deep NO3 at Near Seattle Offshore.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/6e87b848-2c79-4ce9-93d9-234b8a6470f4" width="800"/><br>Fig 20. Summer surface and deep chlorophyll at Near Seattle Offshore.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/bbb28efa-a6da-42e5-a262-c899f3410270" width="800"/><br>Fig 21. Summer surface and deep NO3 at Saratoga Passage Mid.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/bb0e8076-c939-46dd-86df-2d9cf549a2a4" width="800"/><br>Fig 22. Summer surface and deep chlorophyll at Saratoga Passage Mid.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/a0da5131-83e5-4d71-bdb0-f46865c7f569" width="800"/><br>Fig 23. Summer surface and deep NO3 at Carr Inlet Mid.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/19f30c06-3b6d-491e-b34b-05aeec06f42c" width="800"/><br>Fig 24. Summer surface and deep chlorophyll at Carr Inlet Mid.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/f7cdfbea-c0eb-4221-8487-05d1d818762a" width="800"/><br>Fig 25. Summer surface and deep NO3 at Lynch Cove Mid.</p><br>

<p style="text-align:center;"><img src="https://github.com/user-attachments/assets/a19d1ea0-eb69-4966-a4d4-65bde9cfc2db" width="800"/><br>Fig 26. Summer surface and deep chlorophyll at Lynch Cove Mid.</p><br>


---

## General Exam Notes

Leaving my General Exam notes here for future reference...

Some good notes from the discussions:
1. Lots of great audience comments - Melissa Moulton mentioned using idealized terminal inlets for hypothesis testing using LO.
2. Mike notes that using "sensitivity" or lack thereof when it comes to Puget Sound nitrogen is sticky, given that the balance of nutrients in the system is equally importance (ref. Mackas & Harrison 1997 figure).
3. Mike recommends using quantitative model assessment, like "model skill score" or RMSE.
4. Mike indicated interest in decadal analysis of river nutrient variability with CT/SA/DO - sent me a nice spreadsheet that he and Ben have workedo on with USGS data from 1948.
5. Mike also indicated interest in other long-term correlations with largescale climate like PDO - e.g., using Race Rocks to correlate both with interdecadal variability in Puget Sound obs + climate oscillation.
7. Comments on "avoiding inadvertant p-hacking" - basically, layout all my data analysis steps.
   * Taylor recommended bootstrapping techniques, using Mann-Kendall trends with Thiel-Sen slope (and checking residuals when using linear-regressions...) - 7/22/2024: doing this now
   * Taylor/Alex recommended instead of "no slope detected" - explain the minimum detectable slope given data, say that slope does not exceed that.
   * Group discussed propagating errors through to final results - e.g. what is the uncertainty on my solubility calculations given CT/SA etc. - 7/1/2024: just doing calculations with measured values then assigning 95% confidence intervals for now
   * Also - listing out all the slopes and uncertainties, comparing slopes across sites, keeping 95% confidence interval on slopes... - 7/7/2024: doing this last point now
   * Investigate "step trends" as well as full time series
   * Consider % change vs. absolute changes, like with stratification!
8. Mike pointed out the importance of winter properties on DO minima...consider this in more expanded analyses.
9. Penn Cove - pull in Ecology data as well + Coupeville wharf
10. Emily Herrington - reach out to for Penn Cove data, especially on mussel growing stuff? - Michelle to connect us

Further reading:
1. [Elmstrom et al. (2024)](https://www.nature.com/articles/s43247-024-01235-8) - nutrient trends
2. Provisional WA water quality standards - Taylor emailed
3. [Brandenburger et al. (2011)](https://link.springer.com/article/10.1007/s10498-011-9129-0) - sediment trends

Homework
1. ~~Check into stratification plot labelling issue - confirmed that I just mislabeled. The stratification is DEEP density less SURFACE density in sigma [kg/m^3]. All indicated trends and interpretations are accurate with regards to my calculations, and that was just a typo. Oops, but at least I didn't totally mess up some simple math!~~ - ylabel typo fixed
2. ~~Better solubility calcs using CT/SA - ref. [Garcia and Gordon (1992)](https://aslopubs.onlinelibrary.wiley.com/doi/abs/10.4319/lo.1992.37.6.1307) per Mike.~~
   * ~~Parker recommended calculating relative contributions of both overtime.~~ - see 7/1/2024 blogpost
4. ~~Make sure I know equation of state specifics better - unit change in temperature vs. salinity impact on density.~~ - same as above
5. Parker HW question - can we do a box model to estimate a respiration rate from observations, say in Penn Cove? Basically, what can change our simple DO decay that I scraped together on the board (~ DO(t) = DO_i*e^(t/T)) where T is the time after which DO(T) = DO_i/e (or the e-folding timescale)?
6. Mike HW question - using LO & SSM rates for settling and POC degradation and mean PS depth/Penn Cove depth/etc., how much organic matter reaches the sediment intact? Does water column or sediment respiration seem to dominate?
7. Taylor HW question - ~~compare linear regression trends to Mann-Kendall~~ (broken out by seasons) and bootstrapping/subsampling vs. simple time-averaging, plot residuals for linear regressions!
8. ~~Taylor fieldwork question - looks like some ADCPs in Penn Cove are possible! Where and how long? What other field data would be helpful in Penn Cove?~~ - meeting with Taylor 7/3/2024



---


## Miscellaneous

Thoughts for posterity:
* Gappy temperature data in SOG - investigate this.
* 1970-2000 data - does it exist? Ask around...(DOE, Mesa Program)
* Am I going to do anything in Strait of Georgia?!


---

## Bookkeeping
* CEE Performance Evaluation - ? oops!
* Vacation - 8/19-8/23
* PECS - 9/23-9/27
  * Registered + booked Airbnb!
 

---

### Looking Ahead:
1. Upwelling data - look into NANOOS NVS (NDBC or the NSF OOI Endurance Array).
2. Are warming events more common in NE Pacific? Paper??? (Ref. [this](https://www.pugetsoundinstitute.org/2023/09/warm-ocean-waters-work-their-way-into-puget-sound/))
3. Keep on Taylor for me to be involved in KC Whidbey sampling...

### Goals For This Week:
1. 

