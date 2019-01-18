# Khehla Malakoane Full Report
---
Table of Contents <br/>
* [Introduction](#Intro)
* [Dataset](#Data)
* [Methodology](#Method)
* [Results](#Results)
* [Discussion](#Disc)
* [Conclusion](#Conc)
---
<a id='Intro'></a>
## Introduction 
Manila is the capital city of the philipines. It is comprise of 17 districts. Manila is the centre of trade and finance in the Philippines. The city has a chronic housing shortage due being densely populated and contains a significant proportion of the population of the country. As historical and architectural aspects is concern the city landscape is not well planned out in supporting a lot of ventures and people.

**Business problem**<br/>
This study will explore the clustering of establishments on different parts of manila to identify current establishment concentration per district. All types of establishments will be inluded from leasure centers to restaurants. 

**Targert Audience**<br/>
Government and Urban Planner. By understanding the current concentration of establishments it can help the in decision making regarding city developments.

---
<a id='Data'></a>
## Dataset
The geographical data used for this study was obtained from [https://foursquare.com/](https://foursquare.com/). Information about different establishments was grathered from Foursqaure. <br/>

Using the the Foursquare API, the informatation of the establishments were retrieved and analyzed.<br/>

![FoliumMap1](./images/FoliumMap1.PNG) <br/>

---
<a id='Method'></a>
## Methodology
The CRoss-Industry Standard Process for Data Dining was employed for this project. 
<br/>
Specifically for *Modeling*, the K-Means Clustering algorithm was used. <br/>
The Elbow Plot method was used to find the Optimal K for the retried dataset.
![CRISP-DM](https://www.kdnuggets.com/wp-content/uploads/crisp-dm-4-problems-fig1.png) <br/>

---
<a id='Results'></a>
## Results

![EstPlot1](./images/EstablishmentsPlot1.PNG) <br/>

The top districts with most establishments retrieved are the following:
- Malate
- San Nicolas
- Ermita
- Santa Cruz
- Binondo
- Intramuros
---
![EstPlot1](./images/EstablishmentsPlot2.PNG) <br/>

There were different types of establishments retrieved using the API. Different establishment types and their relatived frequency to other types were displayed using the Tree Map plot <br/>

---
![EstPlot1](./images/EstablishmentsPlot3.PNG) <br/>
It can be infer that majority of districts were comprise of the following establishments: 
1. Chinese Restaurant
2. Coffee Shop
3. Fast Food Restaurant
4. Filipino Restaurant
5. Convenience Store
6. Pizza Place
---

### K-Means Clustering
The implementation of the K Means needs a declaration of a K or the number of clusters.<br/>
However, using the Elbow Method an optimal K can be determined. The optimal K found using the method is 4 clusters.<br/>

![Optimal](./images/Optimal.PNG) <br/>

---
Applying the Clustering methodology. The map below shows the geographical relationships of the identified clustered districts.<br/>
![FoliumMap2](./images/FoliumMap2.PNG) <br/>

---
### Cluster 0 
Composed of the following:
- Paco
- Santa Mesa
- Port Area
- San Miguel
![Cluster0Table](./images/Cluster0Table.PNG) <br/>
*Geographically, cluster 0 was near bodies of water.*
<br/>*San Miguel, Santa Mesa and Paco is along Pasig River.*
<br/>*While the Port Area is in front of Manila Bay.*
![Cluster0Plot](./images/Cluster0Plot.PNG) <br/>
<br/>The **Top 5 establishments in cluster 0** were the following
1. Fast Food Restaurant
2. Convenience Store
3. Pizza Place
4. Filipino Restaurant
5. Grocery Store
---
### Cluster 1
Composed of the following:
- Malate
- Ermita
- Binondo
- San Nicolas
- Santa Cruz
- Intramuros
- Sampaloc
- Quiapo
![Cluster1Table](./images/Cluster1Table.PNG) <br/>
*Geographically, cluster 1 is the largest compare to other clusters.*
<br/>*Districts is along PNR rail tracks.*
<br/>*Most of the districts in this cluster is in zones with more establishments*
![Cluster1Plot](./images/Cluster1Plot.PNG) <br/>
<br/>The **Top 5 establishments in cluster 1** were the following
1. Chinese Restaurant
2. Coffee Shop
3. Filipino Restaurant
4. Fast Food Restaurant
5. Pizza Place
---
### Cluster 2
Composed of the following:
- Tondo
- Pandacan
![Cluster2Table](./images/Cluster2Table.PNG) <br/>
*Geographically, cluster 2 is the also near a body of water.*
<br/>*There were less establishments surrounding the districts in this cluster*
![Cluster2Plot](./images/Cluster2Plot.PNG) <br/>
<br/>The **Top 5 establishments in cluster 2** were the following
1. Fast Food Restaurant
2. Convenience Store
3. Grocery Store
4. Snack Place
5. Filipino Restaurant
---
### Cluster 3
Composed of the following:
- San Andres
![Cluster3Table](./images/Cluster3Table.PNG) <br/>
*Geographically, cluster 3 is only composed of one district.*
<br/>*This cluster is not near a body of water relative to other clusters*
<br/>*It is near more establishments compare to Cluster 1 and 2*
![Cluster3Plot](./images/Cluster3Plot.PNG) <br/>
<br/>The **Top 5 establishments in cluster 3** were the following:
1. Convenience Store
2. Fast Food Restaurant
3. Hotel
4. Chinese Restaurant
5. Coffee Shop
---
<a id='Disc'></a>
## Discussion
<br/> Using the Foursquare API, different establishments and geographical locations can be retrieved.
<br/> However, one limitation of the data is that it is user based. Locations which are less popular to Foursquare useds can have less or thin dataset.
<br/> Cluster 2 is consist of district with the fewest establishments. The data for the Cluster 2 for the districts of Pandacan and Tondo was the smallest with 16 and 24 retrieved establishments, respectively.
<br/> Geographically, Majority of big districts in big clusters were either near bodies of water or near rail road tracks. This suggests that most business build their establishments near possible transportation routes.
<br/> The districts Cluster 0 were near bodies of waters. Majority of Establishments can be found on Cluster 1, which is along the Rail Road Tracks.
<br/> Food-related and Convenience Store were the majority establishment types located in manila. This suggests that food-related business is very abundant in each districts. The most frequent food establishments were Chinese Restaurants.
<br/> Since manila is consist of residential areas convinence store is also an abudant business venture.

---

<a id='Conc'></a>
## Conclusion 
<br/> This project focused on geographical data to implement the CRISP-DM pipeline in exploring the establishment concentration in the 17 District of Manila Philippines.
<br/>Using the K-Means clustering algirithm and Elbow plot method, an optimal 4 clusters were identified and analyzed.
<br/>It was found that most clusters were near bodies of water or rail road tracks. The most frequent establishment types were Food-related and Convenience Store. 
<br/> The governement can utilize this results to check the sustainability of the number of establishments on the identified clusters.

---