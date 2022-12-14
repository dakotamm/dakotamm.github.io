# Chugging Along

### Goals From Last Week:
1. Use cas6 (LO) grid - learn how to use/plot/etc.
2. Begin to understand LO daily output formats + lowpass tidal-averaging.
3. Bring down and organize DFO data from CIOOS ERDDAP server (take notes).
4. Get Endnote up and running.
5. Meet with Kate (scheduled for Tuesday, 11/22/2022).

### Completed Goals:
1. Started working with cas6 (LO) grid - figuring out .nc files/plotting.
2. Attempted "extract lowpass" function with latest LO data on Perigee - debugging.
3. Downloaded DFO data - working on cleaning/adding calcutated values to match UBC database.

---

## (Anticlimactic) Updates

From last week, we changed direction somewhat to work with LO output to develop hysographic methods for estimating state variables. First tasks were to dig into the LO outputs and LO grid (cas6). As a starting point, I attempted the following items:

1. Plot the cas6 grid - most of my time was spent learning how to read in NetCDF file formats and variable naming conventions. I haven't gotten to visualization yet.
2. Run an extract lowpass method on LO data on Perigee to get tidally-averaged results. This will be useful for estimatation methods but was also intended as a pathway to get me into working with LO outputs. I was able to locate existing methods, get set up to run on my Perigee machine, work through some kinds, but I ran into a bug that has blocked me:
  * "*** Missing required argument to extract_argfun.intro(): gtagex" - I have the correct pathways set up on Perigee (to the best of my knowledge). So I'm pointing at the right function in lo_tools. It looks like this function shouldn't need an input argument and doesn't in the extract code. I'm sure I'm missing something :P

In parallel, I've been efforting getting DFO data from the ERDDAP server and into a usable format similar to the UBC set. I ran into timeout issues on the ERDDAP server with formats other than CSV... Might be an issue with my RAM? In either case, I have the huge CSVs and documentation of how I got them. The next step is getting them into a nice dataframe and then applying similar calculations used in the UBC dataset (mainly for ease of use and being able to not overhaul all existing processing code).
  * Note: UBC added calculated columns not present in original code. I'm planning to replicate this.
  * Any particular place I should store the raw data/working README/intermediate dataframes?

Kate and I are meeting tomorrow - I'm excited to get an intro to her methods!

---

### Issues/Questions:
1. I'm trying to sort out workflow through LO_user, LO_data, LO_output, etc. when working locally/on my repo... Confirming that "LO_user" should be copy of whatever I'm working on that would otherwise be in the LO folder? Other folders I copy and work within those, which are not connected to a repo...
2. **Shift meeting to Tuesday next quarter?** Confirmed!

### Looking Ahead:
1. Continue with cas6 (LO) grid - learn how to use/plot/etc.
2. Continue to build understanding of LO daily output formats + lowpass tidal-averaging.
3. Clean/organize DFO data from CIOOS ERDDAP server.
4. Get Endnote up and running - lit. review + notetaking.
5. Meet with Kate (scheduled for Tuesday, 11/22/2022).

### Goals For This Week:
1. Familiarize with cas6 grid.
2. Continue to build understanding of LO daily output formats + lowpass tidal-averaging (after).
3. Clean/organize DFO data from CIOOS ERDDAP server.
4. Get Endnote up and running - lit. review + notetaking.
5. Meet with Kate (scheduled for Tuesday, 11/22/2022).
