# Restaurant Recommendation System Using Hybrid Filtering Methods
## Problem Statement
The problem statement we will be working on for this mini project is to build a restaurant recommendation system by using a Hybrid Filtering method. A combination of content-based and location- based filtering methods has been employed in providing personalized recommendations to the user.
## Proposed Approach
•	**CONTENT BASED FILTERING**
Finding similar restaurants based on cuisine preferred by user using TF-IDF and cosine similarity score.
•	**LOCATION BASED FILTERING**
A dataset with all the locations of the restaurants in the dataset, along with their latitude and longitude values is created. 
We form clusters of all close by locations using 3 clustering algorithms and choose the most accurate one.
Using K-Means Clustering, clusters of nearby locations are formed using Euclidean distance as the distance metric for inter-cluster distance. The restaurants recommended using content-based filtering
technique is made even more personalized by recommending only those restaurants belonging to the same cluster as that of the location mentioned by the user.
•	**FUZZY LOGIC**
The recommendations would be even more accurate if the recommended restaurant has an overall good mean rating in comparison to other restaurants. It is completely uncertain(fuzzy) as to what value of mean rating is considered to be a really good, average and poor recommendation. We use fuzzy logic to tackle this issue.

## Steps for Execution:
1. Download the attached python files- RestaurantRecommendation.ipynb and ClusteringMethods.ipynb, and the Location dataset-location.csv
2. Use kaggle for execution
3. First we will check which clustering algorithm is optimal
4. Open ClusteringMethods.ipynb in kaggle
5. Using the **+ Add Data** option import the location.csv dataset
6. Execute each block of code in the notebook in order
7. The clustering algorithm with the highest silhouette score is chosen
8. Open RestaurantRecommendation.ipynb on kaggle
9. Using the **+ Add Data** option import the location.csv dataset and the restaurant dataset- https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants
10. Execute each block of code in the notebook in order
11. recommend2 function accepts two arguments- restaurant name and location. It will recommend users the restaurants that are similar to the restaurant entered by the user and located nearby the user's preferred location
12. newUser function is used if the user is new to the city and has no information about restaurant names. So they can just enter their preferred location and get top restaurants from the nearby areas.
