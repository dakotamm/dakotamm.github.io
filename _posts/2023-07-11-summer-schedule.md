# Summer Schedule

### Goals From Last Meeting:
1. CEE PhD performance review - meet with Alex Thursday 6/29/2023.
2. Summer schedule.

### Completed Goals:
1. CEE PhD performance review.
2. Summer schedule.

---

## Planning

**Guiding Science Questions & Objectives:**
* Using observational data, how has dissolved oxygen changed over time in the Salish Sea?
  * What are the spatial and temporal patterns? Are certain areas exhibiting similar or disparate trends?
* Can we observe trends in hypoxic volume using observational data? How confidant are we in these estimates?
  * What tools do we need to understand uncertainty?
* What are we limited by in areas that are predicted to have high incidence of hypoxia?
  * Do we need more observations? Can we plan this?
  * Do we need more modeling?
* Can we explain any trends using observations and theory?
* Are there specific areas that should be studied in more depth, such as Penn Cove, Lynch Cove, etc.?
* Compile all available observational data for these tasks.
* Build datasets for model evaluation and intermodel comparison.

 
**Some Broad Notes:**
* I'd like to complete my PhD by Spring 2026 (or earlier!). During this time:
  * I want to hone data science skills via the CEE Data Science Option certificate (requires ~2 more classes).
  * I want to improve public speaking and grow overall confidence in my work and ability.
  * I want to become more proficient at coding and graphic design.
  * **I hope to get some experience using LiveOcean and ROMS for future job opportunities.**
  * **I hope to get experience scoping and potentially conducting meaningful fieldwork.**
    * There may be opportunity to do this with WWU faculty in some capacity.
    * Can we broach the idea of tagging along with King County again?
* I'd like to do my General Exam in Spring 2024.
* Concurrently, I'd like to aim for my first publication (Spring 2024).
* Potential conferences:
  * OSM 2024
  * PECS 2024

### This Summer

**Big Picture:** I want to dig into the data and start understanding some trends, or perhaps lack thereof. There has been discussion regarding more advanced statistics to understand uncertainty; this is something that I'd like to let simmer while I begin digging in more. (Also, the UW Stats department doesn't resume consulting until Fall. It seems like an interesting idea to pursue at that point.) By the end of summer, I'd like to come up with a hypothesis that may form a dissertation chapter regarding trends in hypoxic volume in the Salish Sea. This may be something to do with differences in trends observed in various regions. *I will be working remote Monday, August 21, 2023 - Friday, September 15, 2023.*

#### Rest of July
1. Data exploration - what can we see so far in DO data? Other state variables? What is the spatial variation?
   * Plot trends in temperature, salinity, wind, upwelling, climate indicators, WWTP, etc.
3. Pull in KC Penn Cove data. Work with model evaluation in Penn Cove with Aurora (scoped July 24-August 18).
4. Investigate and incorporate all available data (e.g., Colius, etc.).
5. Continue to track uncertainties and think toward further analysis.
6. Literature review - especially Stramma et al. (2008) & (2010) (with Greg Johnson) to understand techniques in using cast data in larger ocean.
7. Reach out to Susan Allen's new post-doc starting some work with observational data.

#### August
1. Continue to work with Aurora on Penn Cove deep dive.
2. Hypothesis formation for Chapter 1/first paper.
3. Continue to pull in all available data.
4. **Learn how to run LO model?**
5. KC update meeting.
6. Remote work on PDT Monday, 8/21 - Friday, 8/25.
7. Remote work from Europe Monday, 8/28 - Friday, September 15.
   * I won't be able to attend our regularly scheduled meetings - could meet at alternative times.
   * Prioritize independent work such as dataset incorporation/model learning?
  
#### September
1. Remote work from Europe Monday, 8/28 - Friday, September 15 (see above).
2. Vet hypothesis for Chapter 1/first paper.
3. ?

### Fall 2023
1. Classes: CEE 464 (Mike's limnology class) + CEWA 565 (Data Analysis in Water Sciences)
2. Hypothesis testing for first paper/Chapter 1.
3. Consulting with UW Stats department.
4. Plan EFM presentation.

### Winter 2024
1. Start work on general exam + confirm three chapters for dissertation.
3. Start on paper draft.
4. **OSM 2024?**

### Spring 2024
1. General Exam.
2. Refine paper for summer publication?

---

## VFC Updates - Zooming in on Puget Sound

After GRC, I have found myself needing to spend a lot of time thinking through various directions that the work needs to go next. Upon talking with Alex, we think the most interesting avenue of exploration is to start trying to make sense of the data instead of focusing on intense statistical analysis (at least for now). I will keep tracking uncertainties via simple differencing between the LiveOcean model history output and LiveOcean using VFC.

First, I've incorporated all of the available data and created a timeseries since 1930. Largely the gaps are due to lack of data availaibility, but I do filter out if basins are beneath a certain threshold (i.e., if there is only one sample in the basin, or if specific samples take up too much of the surface domain). Figure 1 shows a time series since 1930 (earliest DFO data).

<p style="text-align:center;"><img src="https://github.com/dakotamm/dakotamm.github.io/assets/55995675/a7a93be9-9d82-440e-9cf7-fc6da9a97c10" width="800"/><br>Fig 1. Regional hypoxic volume in the Salish Sea since 1930.</p><br>

Error bars, as previously discussed, are based on the comparison of 2017 LO output and LO casts using VFC during 2017, and are applied per month. From the effort for GRC, we know that the data is somewhat sparse and that in order to understand the trends, I'll need to look at  factors that might influence DO. This may be challenging to do in the whole basin at once. Zooming in on the different components of Puget Sound unfortunately loses a significant portion of the data range, since that data is currently not incorporated if it exists. I note that the error bars in this plot seem a little off - *this merits further investigation and will be revised once I debug*.

<p style="text-align:center;"><img src="https://github.com/dakotamm/dakotamm.github.io/assets/55995675/b38c62f4-82c5-42dd-bb68-ba6f35a49a07" width="800"/><br>Fig 2. Puget Sound regional hypoxic volume in the Salish Sea since 2008.</p><br>

Further, identifying areas of interest (such as Whidbey Basin and Hood Canal) will further narrow my search for trends and their explanations (see Figure 3).

<p style="text-align:center;"><img src="https://github.com/dakotamm/dakotamm.github.io/assets/55995675/70fb5fff-954f-47dd-88fd-9fd339cd13f6" width="800"/><br>Fig 3. Hood Canal and Whidbey Basin hypoxic volume in the Salish Sea since 2008.</p><br>

I acknowledge that there is a whole lot of literature out there and I'm not the first person to invent this wheel! So I'll be dedicating some time to reading (especially Greg Johnson's work in the big ocean).

Broadly, next steps are to continue this literature review and continue the observational data exploration, finding other state variables that may covary with hypoxic volume (such as temperature, salinity, wind, climate indicators, WWTP, etc.). Also, I will effort pulling in KC Whidbey Basin data and then seeking to incorporate more data sources.


Some VFC To-Dos For My Own Reference:
* Investigate differences in time-binning.
* Refine statistical understanding and presentation of errors and biases - what's the best way to do this?
* Conduct analyses of different domains, time periods, and state variables of interest.
* Continue refinenement of codebase and work towards making it more time efficient.
* Clean and incorporate more data (especially KC Whidbey Basin data).
* Work with Ben/Aurora on what I can build to be helpful!

---

## Bookkeeping 
* August 21 - September 15, 2023 remote work...

---

### Issues/Questions:
1. Common error estimation methods + statistical bias/error - need lit. review.
2. Organize literature - Endnote?

### Looking Ahead:
1. Digging into Whidbey Basin/Hood Canal.
2. Start pulling Whidbey Basin data.

### Goals For This Week:
1. Different lenses for analyzing trends - seasonal, avg. below 40m DO, T/S analysis, etc.
2. Data cleaning for KC/Whidbey Basin data.
