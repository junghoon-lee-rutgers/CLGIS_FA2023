# Assignment 8
Command-line GIS, Fall 2023
Junghoon Lee

## Schools and School Districts in Hudson County, NJ 
This [map](school_districts_sending_receiving.html) shows municipalities sending their students to school districts other than their own K-12 districts.

- Data sources
  - Enrollment Data (2021): American Community Survey (via census API)
  - School district boundaries (2021): [National Center for Education Statistics](https://nces.ed.gov/programs/edge/Geographic/DistrictBoundaries)
  - Muncipal boundaries (2021): [NHGIS](https://www.nhgis.org/gis-files)
  
- Data Processing
  - I used geoprocessing tools (buffer, clip, intersection, and dissolve) to find which school districts contain which municipalities.
  - To identify the [sending-receiving relationship](https://en.wikipedia.org/wiki/Sending/receiving_relationship#:~:text=A%20sending%2Freceiving%20relationship%20is,part%20of%20a%20historical%20relationship.) between localities and school districts, I identified which grades each municipal school districts does not have, which intersecting school districts can supplement the lack of grades, and estimated the relationship between the municipalities and school districts.
  - Using the estimated sending/receiving relationship, I calculated the number of sending students and the fraction to the total students for each NJ municipality.
  - In the interactive map, I included my own estimation of the relationships as links between the centroids of municipalities and school districts.

### Static Map
<img src="static.png" ="1025" ="700">

### Interactive Map
<iframe src = 'school_districts_sending_receiving.html' width = 800 height = 800> </iframe>
