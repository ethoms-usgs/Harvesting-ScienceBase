# Harvesting ScienceBase
[ScienceBase](https://www.sciencebase.gov/catalog/) is a platform for storing and serving USGS data. One benefit of using ScienceBase for the storage of geospatial data is that uploading shapefiles, geotiffs, or ESRI service definition files will automatically result in the creation of web services. I wanted to explore the possibility of collecting services found within a ScienceBase community and exposing them to some sort of map-based portal for easy discovery.

The Alaska Science Center uploads copies of all data releases published by ASC-researchers to a community called [USGS Alaska Science Center - Data Release Backups](https://www.sciencebase.gov/catalog/item/56b3ee22e4b0cc79997fb64b). The Jupyter notebooks in this repo contain examples of using [sciencebasepy](https://github.com/usgs/sciencebasepy) to navigate this community to search for web services and prepare documents or data to be used with other applications; [TerriaJS](https://terria.io/) and ArcGIS Online (AGOL), in particular.

```sb-items-2-terriajs-data-catalog.ipynb``` is an example of writing a JSON-format 'data catalog' file for TerriaJS. This is my preferred portal application but I don't have a stable instance of TerriaJS with which to use the data catalog. 

```sb-items-2-agol-categories.ipynb``` navigates the parent-child tree of a community and builds a 'category schema' which is used to define nested category labels at an ArcGIS Online group.

```register-sb-with-agol.ipynb``` searches for services at a community and register them as new items at AGOL, grouping them within a folder in the user's content, sharing them a group, and assigning group categories to the items. The SB community must be the same one referenced in ```sb-items-2-agol-categories.ipynb``` in order for the categories to make sense.
