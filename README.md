# DC Zoning Exempt buildings

For this assignment, a python script was implemented in a Google Colab Notebook to manipulate spatial and tabular data for the specific purpose of mapping zoning exempted buildings in DC that provide affordable housing units. Planned Unit Development (PUDs) and affordable housing data were obtained from [Open Data DC](https://opendata.dc.gov/). A crosswalk was additionally provided by the instrutor.  A folder structure was created in google drive and all data was uploaded to the input folder. It is important to note that in the Google Colab Notebook, the file name associated with the PUDs data was updated to match the name of the .shp file in the input folder. 

While it is true that open access to spatial data has improved in recent years, data will not always be published in a spatial data format. Tabular data such as .csv files are still commonly used file formats that may contain spatial information. In this excercise, the affordable housing data in the .csv file format was converted into a GeoDataFrame. This was done by adding a geometry column and writing the latitude (X) and longitude (Y) to a POINT object. The resulting GeoDataFrame was then joined to PUDs polygons based on their spatial relationship (intersection) so that all the zoning and affordable housing information exists in the same table. In order to easily interpret the zoning category, the crosswalk was used to convert this into the actual name of the category (Commercial, Residential, or Other/Mixed Use). Only buildings that had affordable housing units (> 0) were considered for the final layer. Finally, the layer was converted to a shapefile and saved to the output folder in my google drive.

[]()
[Link to Map](https://rskearney.carto.com/builder/cf48980a-acf5-4f21-a6fe-119f91d76bef/embed)
