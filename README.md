# satellite-image-training

The amount of data processed is proportional to the size of the input raster file, hence
very large files may cause out-of-memory errors and significant slowdowns. Large raster files
may have regions where very few or no polygons are present, thus all tiles generated from
those regions contain mainly background class. In other words, there is a significant class
imbalance (more background pixels than foreground), and we do not need to keep all
background tiles. Therefore, tiling the whole raster file is inefficient.
For the input raster file, the program generates new cropped raster files for each RoI (Region of Interest), and corresponding shapefiles in a way that most of the
background data have been removed as much as possible while the new cropped raster files contain most of the polygons on the image.

<img> ![image](https://user-images.githubusercontent.com/19760199/136580096-c2a3f5a9-57bd-4a04-a70d-c34fec781792.png) </img>
<img> ![image](https://user-images.githubusercontent.com/19760199/136579990-15cf02f2-0051-4d02-9773-ce728873025b.png) </img>
