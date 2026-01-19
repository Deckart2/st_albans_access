## Presentation Outline:

Title: Measuring Spatial Access to Resources at Scale 

## Who am I:
- Graduated from Brophy College Preparatory in Phoenix, AZ
- Studied a mix of Geography, Public Policy, and Computer Science
- Data scientist at the Urban Institute:
   - Build tools to support communities' support fair resource allocation and upward mobility from poverty
   
## Run of Show:
- Motiation: Why is spatial access important
- Present on some spatial and demographic data analysis concepts
- Break you all in three groups to have you all consider a spatial access measure
- We will share out to the group
- I will present a bit on how we think about these things in practice for a piece of software I have co-built and work on at Urban

## Motivation:
- Government resource allocation: Identify disparities or suitable opportunities for investment
- Business (location intelligence): Determine underserved markets

## Key concepts

### Point and vector data 
- Point data - used to represent a single location:
  - Ex: Location of post offices, bus stops, libraries
- Polygon data - used to represent a shape:
  - Ex: State borders

### Census tracts
- [Define census tract]
- Often closely aligned with a concept of a "neighborhood" in cities
- Rural areas: they are much larger
- Screenshot of St. Alban's census tract
[create map using tmap and leaflet showing boundaries of census tract]

### Centroids:
- Informally: the center of a polygon 
- A bit more formally: Geometric center or "average location" of a polygon
[image of centroid]

## Spatial Access Methods:
- Break into three groups
- You all review the next three slides independently: they will tell you how to calculate the approach
- Your jobs are to:
  - Review and understand the approach
  - Determine, in the abstract, the strengths and limitations of the approach
  - Identify an example for when the method would be suitable and unsuitable
  - Nominate a group representative to share out your results


## Method 1: The container method
1. Count the number of points in a given census tract
2. Treat all points in the polygon as accessible to residents of the census tract and all points outside the census tract as inaccessible
3. Optionally, divide number of points by the population of the tract to get a "resource per person" measure

## Method 2: Minimum Distance
1. For each tract, start with a tract centroid
2. Calculate the minimum distance to a given resource

## Method 3: Gravity Potential
1. Start with the tract centroid:
2. For the tract centroid, 
  - Calculate the distance to each resource and divide that by the square of the distance
  - Sum those values

Formally, this looks like: $access_i = \sum{\frac{1}{d_j ^2}}$


## Discussion
- Present method
- Strengths
- Limitation
- Use case that demonstrates strenght
- Use case where measure is inappropriate

## Example:
[libraries in dc calculated using each of the three methods]

## Spatial Equity Data Tool:
- Free software that lives on Urban's website
- Built to respond to local government desires to advance racial equity and align with "smart cities" goals
- Cities want analytics but may not have support to calculate it
- Or they different definitions of access / equity
- Use container method


[demo]




