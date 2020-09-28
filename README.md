# Data_visualization
This project presents the sample of usage of altair for data visualization.

## Visualization weather data 

### Import libraries 

'from vega_datasets import data
import os
import altair as alt
import numpy as np
import pandas as pd'

### Load dataset

'seattle = data.seattle_weather()
seattle.head()'

### Relationship between precipitation and date with respective to weather and the size of point by amount of precipitation

'alt.Chart(seattle).mark_circle().encode(
    alt.X('date', title="Date",scale=alt.Scale(zero=False)),
    alt.Y('temp_max',title="Temp max", scale=alt.Scale(zero=False, padding=1)),
    color='weather',
    size='precipitation',
    tooltip=[alt.Tooltip('date'),
            alt.Tooltip('temp_max'),
            alt.Tooltip('weather'),
            alt.Tooltip('precipitation')]
).properties(width=500,height=400,title="Max tempreature vs date against weather and precipitation")'

![Example screenshot](./images/weather/visualization.png)

## Visualization price data 
