# Project: (How) does "the weather" affect Ride performance ?
The aim of the project is to figure out if, and how, "the weather" (i.e. climate data in the likes of humidity, precipation, temperature, ...) affects the stats recorded on strava.

<img
  src="./ProjectIdea.png"
  alt="Coordinate system showing a pinkish and a greenish line. The lines are annotated with weather icons"
  style="display: inline-block; margin: 0 auto; max-width: 200">


## Data
<span style="background-color: #555555">! As I dont want to give away my personal data I will only describe, but not provide the datasets I will work / have been working with !</span> 

For the analysis "wheather" and ride data is needed. Hence this section is divided into a part that discusses the ride data and one discussing the "wheather" data. The raw data is compiled from these sources:

* ☔ Historical Weatherdata from Germany (based on DWD API): https://brightsky.dev
* 🚲 Ride statistics: https://www.strava.com/api/v3/athletes/{athleteID}


### Strava
---
#### Which rides are relevant?
To allow for comparison of different rides, segments have to be found that are ridden quite often. A side contraint that arises from the choosen weather-API limits the rides in question to germany only. For an initial overview the Strava heatmap helps a lot (https://www.strava.com/athlete/heatmaps):

<img
  src="./Heatmap.png"
  alt="Strava heatmap"
  style="display: inline-block; margin: 0 auto; max-width: 200">

By providing the heatmap, Strava already did a lot of the heavy lifting needed for identifying the segments / route in question, however:

#### Which stats are relevant?
- averageSpeed: this metric is used quite often to determine the "performance" of a rider

### BrightSky
---
#### Which "weather" data is relevant?

### Structure of the preprocessed (aka "wrangled") data
The data is available as JSON-file
```json
{ 
  "SegmentId": {
    "lat_long_Start": "00.00..°",
    "lat_long_End": "00.00..°"
    "RideId": {
      "timestamp": "YY-MM-DD HH:MM:SS"
      "Stats": {
        "averageSpeed": "00.0 kph"
      }
      "Weather": {
        "avg_temperature": //the average temperature between start and end coordinates of the given segment
      }
    }
  }
}
```
## Methodology
* Statistics:
  * Test wheter ride data is statistically relevant (i.e.: carries the desired information and is representative)
## Results

