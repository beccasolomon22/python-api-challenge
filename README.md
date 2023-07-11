# python-api-challenge

## Sources

1. Starter Code provided in the asssignments file
2. Stack Overflow was a great help when experiencing error messages
3. I occasionally used Chat GPT to help edit code to fix errors
4. Assignment description

# Project Overview as Described in Assignment:

Use your knowledge of Python and API calls to access the weather information of a list of randomly generated cities across the world. Compare different types of weather with the cities closeness to the equater. Perform linear regression on the comparison scatter plots to determine correlation. Lastly, using the same city data, create a map with all the cities marked and narrow down the list of cities based on weather conditions.

## Tools Used
1. Python
2. Pandas
3. Matplotlib
4. Requests
5. Numpy
6. API

## WeatherPy Findings

After running the API call and converting the data to a dictionary then to a dataframe, I separated the data by hemisphere and created multiple scatter plots to compare Latitude to a number of different factors to see if there was a correlation between the two.

### Latitude VS Max Temperature

#### Northern Hemisphere
![]()

#### Southern Hemisphere
![]()

Both of the r-squared values for the Northern and Southern Hemispheres are above .4, therefore indicate a correlation between Max Temperature and Latitude.

For the Northern Hemisphere, there is a negative correlation from the latitude values of 0 to 80. This means that the further away we get from the equater, the colder it will get. (Or more literally, the further from the equater the lower the max temp)

For the Southern Hemisphere, the is a positive correlation from the latitude values of -60 to 0. This means, despite the opposite correlation from the Northern Hemisphere, that the further we get from the equater, the colder it will get. (Or more literally, the closer to the equater the higher the max temp)

### Latitude VS Humidity

#### Northern Hemisphere
![]()

#### Southern Hemisphere
![]()

With a .005 r-squared value in the Northern Hemisphere and a .05 r-squared value in the Southern Hemisphere, there is a low correlation between Latitude and Humidity.

Despite low correlation, the Northern Hemisphere seems to indicate a slight upward trend and the Southern Hemisphere indicates a slight downward trend. Along with the visual of both graphs having a large amount of points towards the top of the graph, we can take these trends as a possibility that there is a wider range of humidity towards the equater.

### Latitude VS Cloudiness

#### Northern Hemisphere
![]()

#### Southern Hemisphere
![]()

With a .000001 r-squared value in the Northern Hemisphere and a .002 r-squared value in the Southern Hemisphere, there is a low correlation between Latitude and Cloudiness.

Despite low correlation, there are still some conclusions we can come to. This low correlation would lead us to believe that cloudiness does not depend on where we are at in regards to the equator. Cloudiness may depend more on other factors besides latitude. For instance, it may be beneficial to look into amount of cloudiness and the landscape or the nearness to the ocean.

### Latitude VS Wind Speed

#### Northern Hemisphere
![]()

#### Southern Hemisphere
![]()

With a .0003 r-squared value in the Northern Hemisphere and a .01 r-squared value in the Southern Hemisphere, there is a very low correlation between Latitude and Wind Speed.

Despite low correlation, there are still some conclusions we can come to. In both Hemispheres, there appears to be far more cities with lower windspeed than higher. It might again be a good next step to compare Wind Speed to other factors besides Latitude. The first factors I would look into would be proximity to large bodies of water and elevation.

With an optimal value of 4 clusters, used KMeans to model, fit, and predict (with the Regular Scaled Data) to group the cryptocurrencies into 4 clusters

![reg_clusters](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/Reg_Clusters.png) 

## VacationPy Findings

Using the PCA scaled data, created an elbow curve to see what is the optimal number of clusters

![pca_elbow](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/PCA_Elbow.png) 

With an optimal value of 4 clusters, used KMeans to model, fit, and predict (with the PCA Scaled Data) to group the cryptocurrencies into 4 clusters

![pca_clusters](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/PCA_Clusters.png) 

## Comparison

Regular          |   PCA
:-----------------------------------------------------------------:|:-----------------------------------------------------------------:
![reg_elbow](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/Reg_Elbow.png) | ![pca_elbow](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/PCA_Elbow.png) 
:-----------------------------------------------------------------:|:-----------------------------------------------------------------:
![reg_clusters](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/Reg_Clusters.png)   | ![pca_clusters](https://github.com/beccasolomon22/CryptoClustering/blob/main/Images/PCA_Clusters.png) 

Although each uses an optimal 4 clusters, we see a stark change between the Regular and PCA clusters. With PCA we see must more definitive clusters, without as much overlap. 

EX: Cluster 2 in the Regular clusters is nestled within cluster 3. However, in the PCA clusters, cluster 2 is completely separate from cluster 3 and there is very little overlap (a small bit of overlap can be seen with clusters 0 and 3)
