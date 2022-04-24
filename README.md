# road_segmentation_data_generation
Generation of road data set for segmentation studies using Google Map Static API

This code generates satellite and road image pairs for segmentation studies using static map services of Google Maps platform. The generation of satellite and mask images are also available in GeoTiff format, if desired. That way, one can use these images in geospatial analysis, as well.

This code is configured to be run in Google Colab platform. In case you would like to use in personal computer, make sure to remove the `!pip install rasterio` part from the code.

## How to use

User defined parameters:
- `API_key` Google Map Static API Key is unique to each user
- `project_name` Name of the project folder that will be created if not exists
- `minLat, maxLat, minLon, maxLon` Geographic bounderies of the area of interest
- `image_size` Size of the image to be downloaded
- `metadata` Google Map Static API Key is unique to each user
- `rectify` To rectify satellite and mask images and produce GeoTiff files (True/False) 

The code is configured to generate the mask imagesd that contains only road information. Randomly selected satellite and corresponding mask images will be downloaded into the project folder with respect to their zoom level. Additionaly, an HTML file that gives the map of the locations of image frames is created inside the project folder. The central coordinates, as well as the corner coordinates, are written into the log file.

## How to cite:

Ozturk, O., Isik, M. S., Sariturk, B., Seker, D. Z. (2022). Generation of Istanbul Road Data Set using Google Map API for Deep Learning-Based Segmentation. International Journal of Remote Sensing, DOI: http://dx.doi.org/10.1080/01431161.2022.2068989.


```
@article{Ozturk_et_al_2022,
	author = {Ozturk,Ozan and Isik,Mustafa Serkan and Sariturk,Batuhan and Seker,Dursun Zafer},
	title = {Generation of Istanbul Road Data Set using Google Map API for Deep Learning-Based Segmentation},
	journal = {International Journal of Remote Sensing},
	year = {2022},
	doi = {10.1080/01431161.2022.2068989},
}
```
