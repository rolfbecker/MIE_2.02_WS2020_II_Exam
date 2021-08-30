# MIE_2.02_SS2021_III_Exam
Overview of exercises guiding your investigation:

* [Exercise 1](doc/ex1.md) Generate a map of the main investigation area.
* [Exercise 2](doc/ex2.md) Generate SMI maps of the counties of interest for the selected dates.
* [Exercise 3](doc/ex3.md) Generate precipitation video in QGIS.
* [Exercise 4](doc/ex4.md) Calculate cumulative precipitation time series.
* [Exercise 5](doc/ex5.md) Analyse cumulative precipitation vs. altitude (from DTM).
* [Exercise 6](doc/ex6.md) Discuss different SMI dynamics in Olpe and Hochsauerlandkreis.
* [Exercise 7](doc/ex7.md) NDVI
* [Exercise 8](doc/ex8.md) Dimension a roof drainage for two new industrial buildings.

## Introduction

The Soil Moisture Index (SMI) is a product from the Drought Monitor of Umweltforschungszentrum Leipzig (UFZ). It classifies the soil moisture in soil moisture index classes (drought classes) according to the long-term local soil moisture distribution. The assignment of a particular soil moisture value to a soil moisture index is not fixed but depends on the history of the local soil moisture distribution over time. Example: A soil moisture of 10% (volumetric) might be classified as very dry at a usually wet location with a higher mean moisture over the last decades but classified as moderate at another location with lower mean moisture. 
Dimension a roof drainage for two new industrial buildings.
You will investigate SMI, precipitation, terrain and vegetation development (expressed by the normalized difference vegetation index, NDVI) as well as potential dependencies among these quantities. The focus area of your investigation is the Sauerland, a hilly region in South-East Nordrhein-Westfalen. 

The report will have the structure of a scientific report with a continuous narrative flow, even if we split the investigation in several exercises to guide you through the task. 

The exercises are organized such that you can use their order to structure your report. Exercise 1 helps you to locate the area of study. You get an idea of the spatial distibution of climate stations with respect of the area of study in terms of longitude, latitude and altitude. 

Then you start exploring the problem statement focussing on soil moisture. In Exercise 2 you will generate four maps displaying the change of soil moisture index (SMI) of the topsoil layer for the four sucessive months May, June, July, August 2017. 

In Exercise 3 you will start exploring possible explanations for the SMI differences found by investigating the precipitation dynamics in NRW. You will produce a video with the QGIS TimeManager and try to determine the prevalent direction of moving rain fronts in June/July 2017.

Afterwards, you will use Exercise 4 to reduce your study area, by analyzing the two counties Olpe and Hochsauerlankreis with strong differences in SMI development during the time period analyzed. 

You will then calculate cumulative precipitation time series to find out if this SMI behavior can be explained by the total amount of rain fallen in this region. Furthermore you will investigate how the total amount of precipitation is related to the altitude of the weather stations. You will use Exercise 5 to explore this approach. 

After having collected all this data you will use Exercise 6 to start integrating and discussing your observations of SMI, precipitation and altitude. 

The next two exercises will narrow your study area even more. In exercise 7 you will explore whether the SMI behavior is also
reflected in the NDVI. For this you will only focus on three municipalities in Olpe county.

The final exercise 8 is related to precipitation but not to drought (a bit off-topic). Two new industrial buildings are planned in the county of Olpe. The water raining on the roofs of the buildings has to be drained. 

## Organisation

### Groups
You can work in groups with 1 to 3 (max) students. Form groups in the Moodle course is [M-IE_2.02 Geoinformatics, WS2020/21](https://moodle.hochschule-rhein-waal.de/course/view.php?id=12408) if you have not done so yet.

### Due Date
The results of the given practical task shall be comprised of a scientific report. 
You have to submit the assignment via Moodle latest by the **2021-03-21 at 23:59 CET** 
(Central European Time Zone, German local time).

### Files to Upload
Each group has to upload one single archive 
(such as zip, 7z or any other common archive format) 
to the relevant upload area in the Moodle course. 
Any other file format but the common archive extensions will be rejected by Moodle! 
Name the archive after your group name, e.g. groupX.zip. 
Have a look at Moodle upload area early. Only one group member has to upload the group archive. 
The archive has to contain:

- Scientific Report as **PDF(!)**,
- any Python code used to download, convert, aggregate or otherwise process data.
- The video of the hourly spatio-temporal precipitation development (exercise 3).
- QGIS projects with your genererated data.
- Other files can be added if useful.
- **Avoid uploading large data sets** (such as Sentinel images) but describe clearly where the data comes from and how to download and process it. **But you have to enable us to redo your work completely**, i.e. we have to know how to get your data and how to process it with your Python scripts and QGIS projects. 

### Structure of your report 

You have to write one continuous report with a story covering all the exercises mentioned.

You have to add a description of who in the group is responsible for which section. Grading will be individual, so make sure to have an equitative
distribution of work.

Even if your report does not need to specifically divide the text into the elements described below,
the elements shall be easy to distinguish while reading the document. 
Your report will be graded according to the criteria mentioned in the following section.

Your investigation is meant to verify or falsify the hypotheses if possible. 
**It is mandatory to follow best practice of structured scientific writing!** 
Structure the text logically. Justify and explain each step. 
Discuss the findings critically, e.g. are data and methods sufficient to give evidence? 
Do not write in a ‘how-to-style’! 
Design the text such that the reader can fluently follow your story without being interrupted 
with unnecessary or locally inappropriate information, 
e.g. larger code segments can be listed in the appendix if necessary.

Your report should contain the following elements:

- **Title page:** Meaningful title (and subtitle if applicable) of the project, 
name and faculty of the university, study program and course name, 
name (and title if applicable) of the supervisor(s), 
working group name, authors’ complete names, **matriculation numbers** and date of submission.

- **Introduction:** Why are you performing this investigation? Why is it important? 
What is its context, i.e. how is it embedded in the scientific domain and how does it 
compare to others’ work? Use citations to show the interrelation. 
Formulate a research question or hypothesis you want to investigate and 
describe your approach in brief. Describe shortly how the paper is structured.

- **Material and Methods:** This section is used to explain the approach in detail. 
How are you performing the investigation? Where is your data coming from? 
Which tools and methods are you using? How are you doing the aggregations? 
Explain your assumptions and decisions. Explain what you are doing to your data.
Consider which level of information is appropriate in this section. 
Example: Describing exhaustively what a GIS would not be acceptable. 
This is common sense and does not support the reader in understanding your message. 
You can give a short explanation in the text and a substantial reference to further information.

- **Results:** Limit yourself to describe your results. 
What are you observing? 
Do not add any aspect which is not resulting from your very own investigation. 
Remember that tables and figures must be correctly labelled. 
When using maps and other types of graphs take care of the captions, labels and scale. 
Drive the reader’s attention to the specific features you are representing with your results.

- **Discussion:** Interpret your results. Refer to the research question or hypotheses. 
Are your results appropriate to verify or falsify the hypotheses? 
Give a clear answer to your hypotheses (If you can’t then explain why). 
Be critical. What are the limitations of your approach? Is it scalable? 
Compare your results with other investigations (other groups). 
Are they in accordance? You must not be biased with an ‘intended outcome’. 
Limit yourself to discuss your results objectively and scientifically.

- **Conclusions and Outlook:** Summarize what you did and your findings. 
What are the lessons learned? If you conducted the research again, 
what would you do differently? 
What should be done by you or others in future to continue this investigation? 
Which are the open questions? **Do not add any new aspects in this section.** 
**The conclusions are about what you investigated in your work and nothing else!**

- **List of References:** Only use sources that you are referring to in your text and of course
the sources of your data. Use primary literature.
You are writing a scientific report, so use a professional citation style.

- **Annex:** You should have at least an annex with your python notebook which should be commented.

- **Statement of Authorship:** Each group member should add a signed statement of authorship 
to the final report. You can use something like this:

	- *"I, <name>, hereby declare that my contribution to the work presented herein is my own work completed without the use of any aids other than those listed. Any material from other sources or works done by others has been given due acknowledgment and listed in the reference section. Sentences or parts of sentences quoted literally are marked as quotations; identification of other references regarding the statement and scope of the work is quoted. The work presented herein has not been published or submitted elsewhere for assessment in the same or a similar form. I will retain a copy of this assignment until after the Board of Examiners has published the results, which I will make available on request"*
	- Notice that you will have to clearly state which parts belong to your contribution.


### Rules and Regulations

- You should at least cover the material of the exercises in order to pass the course.
- Good grammar, spelling and technical writing are expected for this report. 
Reports showing very poor language skills or largely incomprehensible text passages 
will fail immediately. The supervisors are not willing waste time with bad text.
- Severe deficits in fundamental requirements such as incomplete title page, 
missing figure captions, unbearable maps, or inacceptable citation style will lead to fail. 
The supervisors are not willing waste time with bad structure.
- You will fail if plagiarism is found for the first time (see next section). 
Further actions will be taken if the behavior is recurrent.
- Late submissions are NOT possible.

### Suspected Cheating and Plagiarism
You will be marked with 0 points in the module if cheating or plagiarism is found out. 
This will be assessed according to the faculty´s Academic Writing Manual section 1.5 
Scientific Misconduct on which plagiarism, fabrication, and falsification are stated 
as misconduct and will be considered cheating. 
(HSRW Faculty of Communication and Environment, 2013)

When a student presents the work of someone else as their work is considered plagiarism and this can be intentional or accidental. 
Plagiarism includes:

- Paraphrasing ideas or work of other authors and presenting them as your own. 
In other words, you are not referencing the author(s).
- Presenting work that has been purchased from any source as if it was yours.
- Copying and pasting material from the internet and presenting it as own work.
## Notes

* https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/hourly/precipitation/historical/
* https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/daily/more_precip/historical/
* https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/
