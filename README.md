# OptimizingARIMAModels-
Optimizing ARIMA Models for Midwest Fire Forecasting: A 10-Year Analysis of NASA FIRMS Data and Environmental Factors

This project was done in November and December 2024 for a CLIMATE 599 final project at the University of Michigan.

We use NASA Fire Information for Resource Management (FIRMS) MODIS and VIIRS-SNPP fire detections, which has detected burns as point data in UTC. VIIRS-SNPP spatial resolution is 375m taken twice daily and available since 2012. MODIS spatial resolution is 250m and available since 2000. Relative humidity data is included as lower relative humidity can lead to greater chances of burns. We include NCEP/DOE Reanalysis II daily average relative humidity data as low relative humidity can increase burn chances. The Landsat-derived USDA National Agricultural Statistics Service Cropland Data Layer with a high spatial resolution of 30m is used for burn landcover types. It’s a geo-referenced, annual landcover raster from satellite imagery and in-situ data. Normalized Daily Vegetation Indices are obtained from the Google Earth Engine catalog’s MODIS Terra Surface Reflectance data, and provide landcover health during times of fire detections. Map and analysis products use the WGS 1984 mercator projection. 

Data:
NASA Fire Information for Resource Management or FIRMS MODIS and VIIRS fire detection points are obtained for the continental U.S. region at the Archive Download page via https://firms.modaps.eosdis.nasa.gov/download/.  VIIRS has 375 m sensor resolution, 250 m imagery resolution that is collected twice daily (VIIRS).  MODIS has 250 m Terra data available from November 2000 and Aqua data available from 20 January 2002, and VIIRS Suomi (VIRRS SNPP) 375 m data available from 20 January 2012, all to present time (FIRMS FAQ).  NASA FIRMS supports an open data policy encouraging use of data and graphics with correct citations.

NCEP/DOE Reanalysis II daily mean relative humidity NetCDF data files at different pressure levels for the continental U.S. and based out of Boulder, Colorado, are taken from the NOAA Physical Sciences Laboratory website via https://downloads.psl.noaa.gov/Datasets/ncep.reanalysis2/Dailies/pressure/.  There are no access restrictions or caveats associated with using the data as long as proper citations are implemented.
Landsat-derived geospatial landcover data layers for 1 January 2009 to 1 January 2019 nationally and at 30 m are taken from the United States Department of Agriculture   

National Agricultural Statistics Service (USDA NASS) website’s Research and Science Cropland Data Layer page and from the customer service staff via https://www.nass.usda.gov/Research_and_Science/Cropland/Release/index.php.  This data is for public access, under public domain, and free to redistribute with no USDA NASS warrant on any conclusions made from the data.

MODIS Terra Normalized Daily Vegetation Indices at 500m are obtained from the Google Earth Engine Data Catalog via https://developers.google.com/earth-engine/datasets/catalog/MODIS_MOD09GA_006_NDVI.  There are no restrictions on the subsequent use, sale, or redistribution of MODIS data and products acquired through the LP DAAC. 

MODIS Combined 16-Day NDVI at 250m are obtained from the Google Earth Engine Data Catalog where There are no restrictions on the subsequent use, sale, or redistribution of MODIS data and products acquired through the LP DAAC and it is available via https://developers.google.com/eartengine/datasets/catalog/MODIS_MCD43A4_006_NDV.   
  
Missing average daily NDVI values for one or two dates per year, except 2013, became linearly interpolated based on assuming a linear trend between the two nearest known data values.  Those dates requiring linear interpolation of missing daily NDVI values were: 26 August and 7 September 2009, 11 August 2010, 19 January 2011, 11 May 2012, 14 March and 12 December 2014, 28 October 2015, 18-27 February 2016, 24 April 2017, and 5 December 2018.  Midwest averaged 16-Day MODIS Terra daily NDVI values filled in the missing NDVI value for 18 February 2016.

Software:
Version 3.3.2 of ArcGIS Pro is used for assigning environmental and atmospheric variables to each fire detection point, as well as for clipping all data to the Midwest region.  It is preserved at https://pro.arcgis.com/en/pro-app/latest/get-started/download-arcgis-pro.htm, available via basic, standard, or advanced license levels and single or concurrent use licensing provided by creator, professional, or professional plus user types and developed openly at https://developers.arcgis.com/.


