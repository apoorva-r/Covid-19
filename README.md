## Covid-19 Government Policy Impact - Data Visualisation Tool 
Completed for the course Interactive Data Visualisation 
# Data
We utilized two datasets for our visualization. The first dataset comes from the Oxford
Covid-19 Government Response Tracker and contains information about a country’s
policies in regard to COVID-19. The second dataset is from “Our World in Data” and
contains case data on COVID-19.

# Oxford Covid-19 Government Response Tracker
This dataset contains information about different policies (e.g.: if schools are closed, public
transport is restricted, etc). There are 42 data points per entry.

We use a subset of data points, namely:
● C1_School closing,
● C2_Workplace closing,
● C3_Cancel public events,
● C4_Restrictions on gatherings,
● C5_Close public transport,
● C6_Stay at home requirements,
● C7_Restrictions on internal movement,
● C8_International travel controls, and
● the StringencyIndex.
The data points starting with C are categorized as “Containment and Closure Policies” and
contain ordinal data with (integer) scales between [0, 2] and [0, 4] . For example,
C1_School closing is defined as:
● 0 - no measures
● 1 - recommend closing
● 2 - require closing (only some levels or categories, eg just high school, or just public
schools)
● 3 - require closing all levels
A detailed overview is given in the data’s codebook . The StringencyIndex, on the other
hand, is an average over those C values, where each point is normalized—prior to
average-calculation—to a scale of [0, 100] .

## Our World in Data
This dataset contains information about the COVID-19 cases (e.g.: total number of
cases/deaths, test capacity, etc) and general information about the country (e.g.: population,
number of smokers, etc). There are 33 data points per entry a
We use a subset of data points, namely:
● total_cases,
● new_cases,
● total_deaths, and
● new_deaths.
This data is obtained from the European Centre for Disease Prevention and Control and is
quantitative.

# User
During the COVID-19 pandemic, it is difficult to keep on track with a country’s policies. Our
goal is to help common people understand the local or central government policies related to
lockdown restrictions. There are plenty of visualizations that are drawn already, but the
majority of them show statistics such as active cases, total cases, fatality rates, etc. There
are not many existing visualizations that effectively illustrate the government policies and
their changes over time. Although there are visualizations that show the stringency index of
all countries over time, we would like to extend it to offer more details related to restrictions
of movement for various end-users.
We would like to set this use case to show the lockdown restrictions of any country including
its policies of different categories as our visualization goal namely information visualization. It
is interesting to know such information during the current pandemic situation and it is not a
very common use case. The list of potential users and few important lockdown policies are
mentioned below.
Potential users of our visualization are mostly the common people that include a normal
person, students, and companies (including small, medium, and large scale business
companies). The tasks that are achieved by these users are described in the Task Analysis
section.

# Task
The main task that is achievable with our proposed visualization is to check the stringency
index of government restrictions and more information about its various policies/measures
during different phases of the lockdown in all the countries. The sub-tasks or atomic tasks
which are possible to visualize are described below:
● A normal person can be able to visualize:
  ○ Whether one should stay at home or not depending on the level of restrictions
  to move outside.
  ○ Whether one can plan or organize public events such as marriages, etc or not.
  ○ Whether public gatherings are allowed or not.
  ○ Whether public transport such as taxis, buses, etc are available or not.
  ○ Whether travel between cities or regions is allowed or not.
  ○ Whether the country borders are closed or not
● Students will be able to see whether they are allowed to go to the schools/colleges
and monitor the change in measures.
● Companies can decide whether they are allowed to open their workplace or not and
monitor the change in government restrictions.

# Visualization Techniques
# Choropleth Map
To represent the Strictness level of all the government policies in the countries or regions,
we developed a Choropleth map with Geospatial data to describe the information concerning
a location in the real world. The Choropleth map is developed by using the "Stringency
Index" data values. This data ranges from 0 to 100 (0: No strictness, 100: Maximum
strictness). Each of the data values representing countries is colored as seen by the display
of the color bar ranging from white for “No strictness” to Red for “Maximum strictness”.
These data values are mapped to color and brightness or luminance as the visual variables.
# Policy Heatmap & Line Graph
To depict the policy measures for a particular country on a timeline along with the corona
cases, we developed a heatmap for the policy information and a line graph for the reported
cases. The heatmap was developed by mapping the date on the X-axis and policy
information ('School closing', 'Workplace closing', 'Cancel public events', 'Restrictions on
gatherings', 'Close public transport', 'Stay at home requirements', 'Restrictions on internal
movement', 'International travel controls' ) on the secondary Y-axis. The policy data shown
by heatmap includes 4 data values (0: No measures,1: Recommended measures,2: Partial
Measures, 3: Strict Measures, 4:Total ban). Each of the data values is colored as shown by
the color bar ranging from yellow for “No measures” to Red for a “Total ban”. The line graph
is plotted in the foreground with the date on the X-axis and mapping the count for each of the
reported cases in the primary Y-axis. The reported cases include,
“New_Deaths”,“New_Cases”,“Total_Deaths” and “Total_Cases”. The coloring for the line
graphs is as per the legend. The visual variables used in this combined plot are color and
brightness or luminance.
# Interaction
Different kinds of interactions involved are:
1. Change of visual variables in techniques
4
2. Exploration of data
Several Interaction Operators were used, they are listed below:
1. Navigation: tabs, vertical/ horizontal scrolling, zoom in/out, Automatic shifting within
tabs.
2. Selection: highlights, masking, moved to center of focus, clicking, box/lasso select
3. Filtering: Date slider, Date Range slider, checkbox, region dropdown, Options
4. Connection Operators: Sharing data of country(name)
These Interactive operators were applied on the following interaction spaces:
1. Screen space
2. Data value space
3. Data-structure space

## Contributors 
Jost Rossel, Mitali Gupta, Subrahmanyam Pottimurthi, Apoorva Ravishankar

## Procedure to run the Application
Step 1: Download all the *.py files into a folder.
Step 2: On your command prompt, run the below command:
    python3 tabs-content.py

## Sources 
1 https://raw.githubusercontent.com/OxCGRT/covid-policy-tracker/master/data/OxCGRT_latest.csv
2 https://www.bsg.ox.ac.uk/research/research-projects/coronavirus-government-response-tracker
3 https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/owid-covid-data.csv
4 https://ourworldindata.org/coronavirus
5 https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/codebook.md
6 https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/index_methodology.md
