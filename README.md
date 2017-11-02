# Indian-Census-2011-
Indian government carries out census every decade. This dataset contains information from the 2011 census with district level granularity on population, gender, literacy, socioeconomic status (electricity,​ ​ mobiles,​ ​ Internet)​ ​ among​ ​ a ​ ​ lot​ ​ of​ ​ other​ ​ dimensions.

# Prerequsites 
```
pip install fuzzywuzzy
conda install basemap
```
# Getting India shape files
The shapefiles for a particular country is a gespatial vector data format the are required for state borders.
The base map holds only the outline hence its a requirement to have this to have state borders defined.
The below link is from where the shapefile for india can be downloaded.

https://www.arcgis.com/home/item.html?id=cf9b387de48248a687aafdd4cdff1127 


## 1.Create​ ​ a ​ ​ geographic​ ​ map​ ​ of​ ​ states​ ​ with​ ​ low​ ​ literacy​ ​ rates
1. Extracting State name, Population and LIterates from dateset
2. Checking for null vlaues 
3. Unique values are found from this dataframe so that all the district are grouped into their respective States
4. The literacy rate is calculated of each state.
5. A threshold value is assumed to below which its low literacy rate.
6. A basemap is created and then the latitude and the longitude is set to crop India out of the world map
7. The states with low literacy rate was to be compared with the state names in the SH file as their case was different, a technique of fuzzywuzzy was used to match the strings and select the states to be colored to imply that they are with low literacy rate.
8. The ploted map is shown below.(i.e, Jammu & kashmir, Rajasthan,Uttar Pradesh,Bihar,Jharkhand,Arunachal Pradesh)

![Alt text](c.png?raw=true "india")

## 2.Fin out most similar districts in Bihar and Tamil Nadu.
1. Extract the dataset for BIHAR and Tamil Nadu 
2. Select Columns (District name,Literate,Agrictultural workers) wrt to both states.
3. Concatenate both the state data
4. Plot a scatter plot of the above datapoints.Each data point rperesenting a district (Red>Bihar and green>Tamil nadu)
5. The data points that overlaps are similar wrt to Agricultural workers and Literates
6. Hovering over the datapoints would display the corresponding district names.
7. Districts that are similar are [Ariyalur(TN) with Lakhisarai(Br)][Tanjavur(TN) with Rothas(Br)][Jamui(Br) with Theni(TN)]

![Alt text](a.png?raw=true "Similar districs")

## 3. How does the mobile penetration vary in regions (districts or states) with high or low agricultural workers.



