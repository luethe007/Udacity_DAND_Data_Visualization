# Data Analyst Nanodegree
# Data Visualization
## Project: Make Effective Data Visualization

In this project, I will create a data visualization from a data set about airline delays.
We will investigate one of the main reasons for flight delays: the National Aviation System (NAS) Delay.

### Summary

I have used Jupyter Notebook (Pandas, NumPy and Matplotlib, file: "data_expl.ipynb", src file: "740509512_72018_80_airline_delay_causes.csv") to wrangle and explore the dataset. The dataset comprises data about US air carriers, airports and occurrences of various types of delays such as late aircraft delay, security delay, etc. I calculated which types of delays impact the airlines the most. The most important delay types are Air Carrier Delay, Aircraft Arriving Late and NAS Delay. In more than 80%, those types are the reasons for delays. I deleted any NaN values and started to draw line plots in Jupyter Notebook. I figured out that the NAS data pattern is interesting as I did not expect to see very big differences across airlines for this type of delay.

What is the NAS Delay?

NAS contains delays and cancellations attributable to the national aviation system that refer to a broad set of conditions, such as non-extreme weather conditions, airport operations, heavy traffic volume and air traffic control.

I decided to create an interactive line plot so that the audience is able to explore the data on their own.

I think that this chart reveals some interesting aspects.
First, the NAS is a very important delay driver.
Second, the NAS delay heavily varies across airlines.
Third, airlines which have widespread flight routes tend to have the same ratio of NAS Delays/Total Delays. Accordingly, we can assume a correlation between the NAS delays and the geographic regions where the airlines mainly operate. This correlation becomes very clear by looking at Hawaiian Airlines and Alaska Airlines. Hawaiian Airlines obviously connects the Hawaiian islands, there is typically not much traffic to be expected and NAS Delays/Total Delays is pretty flat only slightly above 0%. However, Alaska Airlines mainly operates on the west coast (Seattle, Portland, LA, San Francsico, San Diego) and the corresponding NAS Delays/Total Delays reached 45% in 2018 (Jan-Oct). The air traffic is very heavy in this region. I did not expect the difference/correlation to be that strong. Nevertheless, this is only a description of the data and the correlation, it does not imply any causal connections.


### Design

The final version is index_final.html (src file: "final_df"), the first version is index1.html (src file: "final_df_3").

I decided to create a line chart as I wanted to illustrate the impact of the NAS on flight dealys for different US air carriers over time. In terms of visual encoding the line plot communicates via slope.
I have chosen an interactive chart in order to let the audience explore the dataset and compare the air carriers.
The interactivity is supported by the color encoding as the color changes by hovering over the lines and the position encoding since the exact data points are interactively shown.

In the first place, I thought of illustrating the major US air carriers American, Delta and United Airlines. Based on the feedback, the biggest change was to incorporate as much airlines as possible. I thought that the audience will only take care about the large airlines, but an interactive chart would make more sense if more data points were added to it and static legends became problematic. The final solution is somewhat in between and could have been managed as well by a legend, but it would already be difficult to not use similar colours for nine airlines.
For future iterations we could intend to gather the data for more airlines to enrich this data visualization. The interactivity gives us the opportunity to manage a very high number of data points.

Furthermore, I have incorporated the changes on the axes. Both axes are more precise and the y-axis starts at zero.

The line colors have been modified. The line color changes from darkblue to lightgrey. The hover effect changes the line to darkblue. This color change makes the visualization more powerful.

I have also added an explanation of the NAS delay because most of the people do not know much about the aviation business.

### Feedback

I shared my first version with some friends, this was the input to improve it:

Person 1: Too few airlines are illustrated. With only a few lines it is better using a legend instead of interactivity.

Person 2: The x-axis should indicate every single year instead of 2 years interval.

Person 3: The color change of the line can be more clear (black and darkblue are too similar). The y-axis could be more precise and should start at 0%.

None of these persons was able to clearly get the message out of it. An explanation of the NAS delay and a y-label would be beneficial to understand the values.

All of these suggestions have been taken into account for the final version.

### Resources

Mike Bostock's Block, Multi-Line Voronoi (https://bl.ocks.org/mbostock/8033015)

Stackoverflow (https://stackoverflow.com/)

Bureau of Transportation Statistics (https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp)
