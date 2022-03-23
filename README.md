# Data Science CoP - Geospatial Data
This repository is a collection of notebooks to get started with geospatial analysis using open government data.  It is companion material for the [geospatial data analysis](https://github.com/hackforla/data-science/wiki/Geospatial-Data-Analysis) tutorial.  The goal is to highlight some of the common idioms with geospatial data.

## Contents of the Repository

This is a fairly standard way to organize a project:

- data - folder for datasets included and generated in various steps

- docs - I usually include some background/idea articles to further explain the ideas

- notebooks folder - contains project notebooks

- README.md and environment.yml - explain the flow and how to create the environment

To provide some focus, we'll develop the project, and explore the idioms, using an economic development scenario.  [Economic development](https://en.wikipedia.org/wiki/Economic_development) covers multiple topics: 1) jobs; 2) education; 3) businesses; and 4) government policies, to name a few.  

For this project we will develop data stories to understand how the State of California and City of Los Angeles support [micro, small, and mid-size enterprises](https://www.investopedia.com/terms/s/smallandmidsizeenterprises.asp).  To make things manageable, we'll focus on neighborhood level analysis.  

Meaningful analysis always starts with questions.  Some of the questions we can answer with open data include:

  1. **Businesses** related:
      - What types of businesses are in Los Angeles?
      - Where are they located?
      - Are there clusters of related businesses?
      
      
  2. **Neighborhood** related:
      - Do neighborhoods have similar distribution of businesses?
      - Does a neighborhood have special programs for businesses?
      - Is the neighborhood in a [Business Improvement District (BID)](https://en.wikipedia.org/wiki/Business_improvement_district)?
      
  3. **Jurisdiction** related:
      - Who are the city council and state representatives for the business?
      - Does the business lie within a Business Improvement District (BID)?
      - Is the business in an [opportunity zone](https://opzones.ca.gov/)?


The notebooks in this project demonstrate common geodata idioms to address these questions:

  ----------------------------
  **Data Basics:**
   - [1-data-wrangling.ipynb](notebooks/1-data-wrangling.ipynb) - Show some basic examples of processing geodata.  I've identified three representative datasets:
   
      - Businesses dataset - csv file from city of la
      - Jurisdictions in LA County - shape file from LA County
      - Opportunity zones from the state - shape file from State of California
      - **Note:** This folder will create geodata from the city url (no need for lfs)

  **Spatial Analysis:**   
   - [2-data-fusion.ipynb](notebooks/2-data-fusion.ipynb) - We'll look at some simple spatial analysis techniques.  Specifically:
   
      - point in polygon techniques to relate businesses and opportunity zones
      - Use choropleth map to show counts and densities
      - Add new datasets for City Council Districts and Business Improvement Districts (BIDs)
      
  
   - [3-combined-details.ipynb](notebooks/3-combine-details.ipynb) - Use ipyleaflet mapping techniques for data exploration/aggregation..
   
      - ipyleaflet-based mapping, overlays, and popups
      - Select one BID (Wilshire) to add businesses to the map
      - NAICS analysis on the business to color code map markers
      - Lot's-o-crap-on-a-map!


     
  **Urban Form:**

   - [4-morphology.ipynb](notebooks/4-morphology.ipynb) - Techniques to compare neighborhoods
   
     - Clustering zones
     - Population measures
     - Street network measures<br><br>
     
     
     
**Note on the data used**

Since this is a github repo I'm trying to avoid having to use lfs.  There are two (bigish) files, the first dataset **should be downloaded** into the data folder before you start.  The second dataset is loaded from data.lacity.org automatically:

  1. [LA Zoning](https://geohub.lacity.org/datasets/lahub::zoning/explore?location=34.018048%2C-118.412136%2C10.23) dataset
  2. [LA businessess](https://data.lacity.org/Administration-Finance/Listing-of-Active-Businesses/6rrh-rzua) pubished by data.lacity.org
  
I have included the rest of the data or what is needed is computed from these two.
 

 

