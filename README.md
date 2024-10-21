# My E-portfolio for machine learning.
Unit 1 Discussion 1 - 

Read the Schwab (2016) article from World Economic Forum and discuss the impact of industry 4.0 on the sector in which you are involved or interested. Instructions 
	Identify a specific incident (not covered in your reading list) where the failure of an information system has had a significant impact.  
	Your post could consider a range of impacts of the failure, including: the implications to customers, the economic cost, the reputational cost, or any other relevant impacts. 
 What is 4.0 the fourth industrial revolution?
 The 4.0 fourth industrial revolution is the integration of intelligent digital technologies in the manufacturing and industrial workplaces. It is a fundamental way to change the way we live, work and relate to each other.  In 2022 a cybersecurity team called safety detectives notified pegasus airlines about a problem they had, which was that they had left a large amount of their sensitive data unprotected. The data contained sensitive information such as flight charts, navigations material, crew PII and software source code. Had a data breach occurred to this data thousands of passengers and flight crew could have been severely affected and their safety compromised. This near incident occurred due to negligence and human error. This could of had severe complications to all the customers, by affecting their holidays, giving out sensitive information and jeopardising the safety of flight crew and passengers.  
References: 
L.Pryimenko (2024) 7 examples of real-life data breaches caused by insider threats. Available at: https://www.ekransystem.com/en/blog/real-life-examples-insider-threat-caused-breaches [data accessed 12th august 2024]. 
McKinsey & company (2022) what are industry 4.0, the fourth industrial revolution, and 4IR?. Available at: https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-are- industry-4-0-the-fourth-industrial-revolution-and-4ir [date accessed 11th august 2024]. 
World economic forum (2016) the fourth industrial revolution: what it means, how to respond. Available at: https://www.weforum.org/agenda/2016/01/the-fourth-industrial-revolution-what-it- means-and-how-to-respond/ [date accessed 12th august 2024]. 


Unit 3 correlation and regression lecturecast





Unit 5 Jaccard coefficient 

Calculating Jaccard coefficient 

The table shows the pathological test results for three individuals.



Calculate Jaccard coefficient for the following pairs:
(Jack, Mary)
(Jack, Jim)
(Jim, Mary)

Jaccard coefficient = 0.33


Jaccard coefficient = 0.67

Jaccard coefficient = 0.75




Unit 6 assignment 


Analytical Report Introduction 
Since its launch in 2008, Airbnb has allowed travellers and hosts to offer more individualised, distinctive travel experiences. 
For this assignment, we developed a business analytics question based on the Airbnb dataset and performed Data Analysis to find the answer. 
What key factors influence the price of Airbnb listings in New York City? 
With this report we aim to understand the primary determinants of listing prices, which can help Airbnb optimise its pricing strategies, identify opportunities for price adjustments, and provide insights for setting competitive prices. 
1 
Data Analysis 
Data Analysis consisted of two tasks: 
	●  Exploratory Data Analysis  
	●  Machine Learning Modelling  Exploratory Data Analysis (EDA)  Exploratory data analysis is crucial in understanding any dataset, providing insights into patterns, trends, and anomalies, and testing a hypothesis to make accurate, informed decisions (IBM, 2021).  Pre-processing  In the data preprocessing stage, we addressed missing values through imputation. We replaced missing values with ‘Unknown’ for fields with minor missing data: name and host_name. The blanks for review-related columns last_review and reviews_per_month, which had around 20% missing data, were identified as corresponding to listings with zero reviews. These gaps were filled with 'No Reviews' and 0, respectively, ensuring data consistency while preserving the dataset's integrity.  Statistical Analysis  

2 
The summary statistics table highlights notable variability in the dataset, especially regarding geographic coordinates and listing prices. The average latitude and longitude values (390.22 and 759.94) appear incorrect, likely due to data errors, with a high standard deviation further emphasising this inconsistency. Listing prices vary widely, from $0 to $10,000, suggesting a mix of affordable and luxury properties. Listings priced at $0 raise concerns about data accuracy, potentially caused by errors or promotions. Most listings (75%) are priced at or below $175, indicating general affordability. The minimum stay requirement ranges from 1 to 1250 nights, reflecting diverse hosting strategies. While the average number of reviews per listing is 23.27, some listings receive up to 58.5 reviews per month, showing varying popularity. Host listings also range widely, from individual hosts to professionals managing as many as 327 properties, with availability varying from occasional to year-round rentals. 
Univariate Analysis 
A deeper univariate analysis of the price variable shows a highly skewed distribution, with most listings priced low and a few extremely high-priced listings creating a long tail. The skewness is evident in the box plot, which highlights several high-priced outliers that raise the mean price. 
 
3 
 
Furthermore, the neighbourhood group and room type are likely significant factors influencing price. As illustrated in the above graphs, Manhattan and Brooklyn have the highest concentration of Airbnb properties, reflecting their popularity and centrality in New York City. Private rooms and entire apartments are the most common offerings on the platform. 
Bivariate Analysis 

4 
Most correlations in the heatmap were pretty weak, except for the one between reviews_per_month and reviews_per_month. To get a clearer picture, correlations were filtered using thresholds of -0.2 and 0.2, and a scatter map was created. 
Here’s what was found: 

● availability_365andreviews_per_month:there’snostrongcorrelationhere. Reviews are pretty evenly spread across different availability levels, with most listings getting fewer than 20 reviews per month, no matter their availability. 
● availability_365andcalculated_host_listings_count:thereisn’taclear correlation. Host listing counts vary across all availability levels. However, there are noticeable horizontal lines, suggesting that some hosts have a typical number of listings (like around 100, 230, and 330). 
5 
● reviews_per_monthandnumber_of_reviews:there’sastrongpositivecorrelation. More reviews per month usually mean a higher total number of reviews, which makes sense - more frequent reviews add up over time. 
● reviews_per_monthandminimum_nights:there’saslightnegativecorrelation. Listings with more reviews per month often have shorter minimum night requirements, suggesting that places with shorter stay options might get booked and reviewed more often. 
● priceandlongitude:anegativecorrelationisevident.Aspricesgoup,longitude values decrease (meaning they move westward). This indicates that, on average, western parts of New York City tend to have higher-priced listings. 
Since the correlation between price and longitude showed the clearest and most interesting trend, further analysis was conducted to test the initial hypothesis. 

6 
As anticipated, the plotted map confirmed that prices increased in the western parts of New York City. 
ML modelling 
Machine Learning modelling assesses data and finds insights to make decisions that enhance company outcomes (Oracle, 2023). 
We used clustering to model the Airbnb dataset. This unsupervised machine-learning technique helps to group related objects by recognising patterns and displaying data. 
The process required three steps: K-prototype for clustering, Mutual Information for feature selection, and tSNE for high-dimensional visualisation. 
By applying Mutual Information, we found factors influencing price and how much information each of them provided about price. 

A high MI score indicates a strong relationship between the feature and the target variable 
7 
We selected the K-prototype algorithm to manage the dataset's numerical and categorical attributes. 
Our analysis grouped 48000 listings into three distinct clusters. The features that greatly influenced these clusters included room_type, longitude, neighbourhood_group, and availability_365. 

8 
Budget listings with greater availability are found in less crowded neighbourhoods, represented in the teal cluster. The yellow cluster shows expensive, premium listings with restricted availability in well-known regions such as Manhattan. The purple cluster depicts mid-range listings, maybe private or shared, with a range of availability, a high number of reviews, and a modest price. 
Clustering research identifies various market segments within NYC's Airbnb listings, providing useful information for strategic decision-making. Using these insights can boost customer happiness and optimise revenue streams. 
Conclusion 
This report presented the examination of key factors influencing the price of Airbnb listings in New York by means of Exploratory Data Analysis and Machine Learning modelling. It provides useful information for maximising pricing strategies by differentiating market clusters according to availability, room type, and location. Better client targeting and more revenue creation can result from these results. 
9 
References 
IBM (2021) What is exploratory data analysis? Available from: https://www.ibm.com/topics/exploratory-data-analysis [Accessed 25 August 2024]. 
Oracle (2023) What is Machine Learning for Analytics? Available from: https://www.oracle.com/in/business-analytics/what-is-machine-learning-for-analytics/ [Accessed 25 August 2024]. 

10 
Appendix EDA: 
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import geopandas as gpd
from sklearn.preprocessing import StandardScaler, LabelEncoder
from tabulate import tabulate
from shapely.geometry import Point
# Importing dataset and
df = pd.read_excel('AB_NYC_2019.xlsx')
# Getting overview of dataset
df.head()
df.info()
# Detecting and Handling with missing values
missing_values = df.isnull().sum()
print(missing_values)
missing_percentage = df.isnull().mean() * 100
missing_percentage.sort_values(ascending=False)
df['name'].fillna('Unknown', inplace=True)
df['host_name'].fillna('Unknown', inplace=True)
missing_values = df.isnull().sum()
print(missing_values)
df.loc[df['number_of_reviews'] == 0, df.loc[df['number_of_reviews'] == 0, 'last_review'].fillna('No Reviews') 
df.loc[df['number_of_reviews'] == 0, 'reviews_per_month'] = df.loc[df['number_of_reviews'] == 0, 'reviews_per_month'].fillna(0) 
print(df.isnull().sum())
df.head()
df.shape
'last_review'] = 
11 
# Calculating summary statistics
df.describe()
summary = df.describe()
summary.to_excel('summary_statistics.xlsx', sheet_name='Summary')
# Plotting variables for univariate analysis
plt.figure(figsize=(10, 6))
sns.histplot(df['price'], bins=50, kde=True)
plt.title('Price Distribution')
plt.xlabel('Price')
plt.ylabel('Frequency')
plt.show()
plt.figure(figsize=(10, 6)) sns.countplot(x='neighbourhood_group', data=df, palette='viridis') plt.title('Number of Listings by Borough',fontdict={'fontsize': 16, 'fontweight': 'bold'}) plt.xlabel('Borough',fontdict={'fontsize': 13}) plt.ylabel('Number of Listings', fontdict={'fontsize': 13}) plt.show() 
plt.figure(figsize=(10, 6)) sns.histplot(df['price'], bins=50, kde=True) plt.title('Price Distribution', fontdict={'fontsize': 16, 'fontweight': 'bold'}) plt.xlabel('Price', fontdict={'fontsize': 13}) plt.ylabel('Frequency', fontdict={'fontsize': 13}) plt.show() 
plt.figure(figsize=(10, 6)) sns.boxplot(x=df['price']) plt.title('Price Box Plot',fontdict={'fontsize': 16, 'fontweight': 'bold'}) plt.xlabel('Price', fontdict={'fontsize': 13}) plt.show() 
plt.figure(figsize=(10, 6)) sns.countplot(x='room_type', data=df, palette='coolwarm') plt.title('Number of Listings by Room Type',fontdict={'fontsize': 16, 'fontweight': 'bold'}) plt.xlabel('Room Type', fontdict={'fontsize': 13}) plt.ylabel('Number of Listings', fontdict={'fontsize': 13}) 
12 
plt.show() 
# Correlation
numerical_df = df.select_dtypes(include=['float', 'int'])
numerical_df = numerical_df.drop(columns=['id'])
corr = numerical_df.corr(method='kendall')
plt.figure(figsize=(13,10))
plt.title("Correlation Between Different Variables\n")
sns.heatmap(corr, annot=True)
plt.show()
positive_threshold = 0.2
negative_threshold = -0.2
positive_correlations = set()
negative_correlations = set()
for i in range(len(corr.columns)):
   for j in range(i):
       corr_value = corr.iloc[i, j]
       colname1 = corr.columns[i]
       colname2 = corr.columns[j]
       if corr_value > positive_threshold:
           positive_correlations.add((colname1, colname2))
       elif corr_value < negative_threshold:
           negative_correlations.add((colname1, colname2))
print("Sets of positively correlated columns:")
for pair in positive_correlations:
print(pair) 
print("\nSets of negatively correlated columns:")
for pair in negative_correlations:
print(pair) 
# Scatter plots
fig, ((ax1, ax2), (ax3, ax4), (ax5, ax6)) = plt.subplots(nrows=3, ncols=2, figsize=(14,10)) 
# Plot 1: 'availability_365' vs. 'reviews_per_month'
13 
plot1_data = pd.concat([df['availability_365'], df['reviews_per_month']], axis=1) sns.regplot(x='availability_365', y='reviews_per_month', data=plot1_data, scatter=True, fit_reg=True, ax=ax1) 
ax1.set_title('Availability vs Reviews per Month')
# Plot 2: 'availability_365' vs. 'calculated_host_listings_count'
plot2_data = pd.concat([df['availability_365'], df['calculated_host_listings_count']], axis=1) sns.regplot(x='availability_365', y='calculated_host_listings_count', data=plot2_data, scatter=True, fit_reg=True, ax=ax2) ax2.set_title('Availability vs Host Listings Count') 
# Plot 3: 'reviews_per_month' vs. 'number_of_reviews'
plot3_data = pd.concat([df['reviews_per_month'], df['number_of_reviews']], axis=1) sns.regplot(x='reviews_per_month', y='number_of_reviews', data=plot3_data, scatter=True, fit_reg=True, ax=ax3) ax3.set_title('Reviews per Month vs Number of Reviews') 
# Plot 4: 'reviews_per_month' vs. 'minimum_nights'
plot4_data = pd.concat([df['reviews_per_month'], df['minimum_nights']], axis=1) sns.regplot(x='reviews_per_month', y='minimum_nights', data=plot4_data, scatter=True, fit_reg=True, ax=ax4) 
ax4.set_title('Reviews per Month vs Minimum Nights')
# Plot 5: 'price' vs. 'longitude'
plot5_data = pd.concat([df['price'], df['longitude']], axis=1) sns.regplot(x='price', y='longitude', data=plot5_data, scatter=True, fit_reg=True, ax=ax5) ax5.set_title('Price vs Longitude') 
plt.tight_layout()
plt.show()
gdf = gpd.GeoDataFrame(
   df, geometry=gpd.points_from_xy(df.longitude, df.latitude),
   crs="EPSG:4326"
)
fig, ax = plt.subplots(figsize=(12, 8))
14 
gdf.plot(ax=ax, markersize=2, c='price', cmap='viridis', alpha=0.6, legend=True) 
ax.set_title('Neighborhood Prices on Map')
ax.set_xlabel('Longitude')
ax.set_ylabel('Latitude')
plt.show() 
ML modelling: 
 
15 
   
16 
 
17 
 

Feedback for unit 6 assignment 

Group 3: Feedback (16/09/24) Assessment of Group 1's Airbnb Project Report 
Substantive Question (5%) 
Commendable: What key factors influence the price of Airbnb listings in New York City? This question was highly relevant and well justified. The focus on price as a critical factor ties directly to Airbnb’s business model. 
Needs Further Work: None. Rational/Arguments for the Business Question (5%) 
Commendable: The group gave a solid rationale for focussing on price, highlighting the competitive nature of Airbnb pricing in New York City. The inclusion of neighbourhoods as a factor adds depth to the analysis. 
Needs Further Work: While the rationale was strong, more attention could have been given to external factors, such as demand fluctuations due to seasonality or significant events in the city. These could have impacted the findings but were not discussed. 
Expected Business Impact (5%) 
Commendable: The group linked their findings to business recommendations. For example, they identified price ranges that yielded higher booking rates and suggested that Airbnb optimise pricing based on neighbourhood-specific trends. 
Needs Further Work: The recommendations could have been enhanced by discussing the implications for Airbnb’s long-term pricing strategy. For example, would lower prices lead to higher occupancy, or is there a threshold where raising prices optimises profitability? 
Methodology (40%) 
Knowledge and Understanding (10%): The group demonstrated a solid understanding of EDA, using correlation matrices and clustering to uncover relationships between variables. Their approach to cleaning the dataset was sound. 
Application of Knowledge and Understanding (10%): The group effectively applied machine learning techniques, particularly clustering, to segment listings by price. 
Criticality (20%): The critical analysis of the clustering results needed to be improved. While the clusters were identified, their business implications were not fully explored. For example, the group could have delved deeper into each cluster's characteristics and explained how Airbnb could use these insights to differentiate pricing strategies for high-end versus budget listings. 
Needs Further Work: The report would have benefitted from comparing different clustering methods or conducting sensitivity analyses to see how changes in variables like amenities or location affect clustering. Additionally, the methodology did not 
1 
clearly explain why certain features were included in the model while others were excluded. 
Visualisations of Results (40%) 
Commendable: The visualisations, particularly the correlation heatmaps and scatterplots, were well-designed and effectively communicated the relationships between pricing, location, and other variables. 
Knowledge and Understanding (10%): The group clearly understood how to use visualisations to show correlations, and their heatmap was particularly effective in highlighting key relationships. 
Application of Knowledge and Understanding (10%): The scatterplots showing price distribution by neighbourhood provided a clear view of how prices vary geographically across New York City. 
Structure and Presentation (20%): The overall structure was solid, but the report slightly exceeded the word limit. 
Needs Further Work: The visualisations could have included more detailed explanations of the findings. For example, the heatmap showed correlations, but the group did not explore why certain variables were more strongly correlated than others, such as the impact of amenities on price. Additionally, some scatterplots lacked proper labelling, making it harder to interpret the results thoroughly. 
Overall Presentation Style (5%) Commendable: The report had a logical flow, with each section building upon the previous one. 
Needs Further Work: The word limit was exceeded, affecting the conciseness of some sections. Additionally, more detailed explanations of the visual data would have strengthened the overall clarity of the report. 
General Feedback 
Your group presented a strong report with well-executed machine learning and EDA techniques. However, the lack of critical analysis of the clustering results weakened the overall impact. The group could have benefitted from a more detailed discussion of the implications of their findings, especially regarding pricing strategies across different neighbourhoods. 
Final Thoughts 
demonstrated a solid understanding of Airbnb’s pricing dynamics in New York City. However, a deeper exploration of the clustering findings and more precise explanations of visual results would strengthen the business recommendations. Ensuring the report adheres to word count limits and providing more critical insights into the results would significantly improve the quality of the analysis. 


Unit 11 assignment ppt
For unit 11 I created a powerpoint to develop a neural network using the CIFAR-10 image dataset. Throughout this powerpoint I explained all about the dataset, I explained about data preprocessing and data splitting including how many images there were in each set. I explained normalisation, and one hot encoding, I showed and explained about the different layers in artificial neural networks, explaining that there are input layers, hidden layers and output layers. I explained the architecture of my models and why we use CNNs. I explained my graphs for my models performance and evaluation. 


Reflection:

Throughout this module I have found myself struggling a lot to understand the tasks asked of me. For unit 1 discussing the 4.0 industrial revolution was quite challenging as I hadn’t heard of it before. So after some research I learned a lot and now understand it a lot more and its impact and importance. 
During unit 3 involving correlation and regression I watched the lecture cast and completed the questions, this gave me an insight into how to calculate it and the different types. 
During unit 5 I completed some calculations involving jaccard coefficient and this took me a while too understand because I could only find explanations using numbers rather than letters and it got me very confused, but after lots of research and ahelp I finally managed to understand it as I had never come across this before, this was learning something new entirely. I feel more confident in using it now. 
During unit 6 I had to complete a team project and we had to design a analytical report. It was hard working as a team because our time zones were different and communication was difficult sometimes because to make a decision or change some work you had to wait for everyone to agree so the process was long. But after some great teamwork we managed to get it complete and all participated our work towards it and got a good mark so I am happy with this. This helped me overcome the difficulties of working as a team. 

During the unit 11 assignment I struggled a lot, it took me a while to understand the code and be able to explain it and understand more about neural network models. I used the CIFAR-10 dataset and had to compare models. Even though I managed to complete the powerpoint I am still a little confused by it so I think I need to continue my research on this and practice more. 

During units 7, 8, and 9. The coding tasks confused me a little bit so I think I need more practice and understanding of how to do this and run different codes to get different outputs. 
Overall this module has taught me a lot of new information but I am aware I still need lots more practice. 
