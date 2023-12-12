**Dataset Used:** https://www.kaggle.com/code/ayushimishra2809/movie-recommendation-system/data?select=ratings.csv
**Code File Name:**
**Interactive Output File name:**

The project had 3 requirements:

**1. To develop a Popularity-based recommender system at a genre level**.
User will input a genre (g), minimum ratings threshold (t) for a movie and no. of recommendations(N) for which it should be recommended top N movies which are most popular within that genre (g) ordered by ratings in descending order where each movie has at least (t) reviews.

**Function Name:** popularity_based_recommendations(g,t, N)
    - Takes 3 arguments - Genre, Rating Threshold, Number of recommendations
    
To perform the same, I followed the below steps:

  **Step- 1:** Calculated the number of ratings and count of ratings based on movie title
  **Step- 2:** Filtered the records for the input genre
  **Step- 3:** Filtered the records for the reviews greater than ratings threshold(input)
  **Step- 4:** Sorted and arranged the dataframe based on average rating
  **Step- 5:** Displayed the final dataframe with Top 'N' recommendations

**2. To develop a Content-based recommender system which recommends top N movies based on similar movie(m) genres.**

**Function Name:** content_based_recommendations(T, n)
    - Takes 2 arguments - Movie Title, Number of recommendations
    
To perform the same, I followed the below steps:

  **Step- 1:** Data was prepared with some pre-processing steps like merging different dataframe, splitting genres as required, dropping columns that are not required
  **Step- 2:** Performed TfidfVectorizer from scikit-learn to convert the movie genres into a TF-IDF matrix. This matrix represents the importance of each word (genre) in each movie's description
  **Step- 3:** Calculated cosine similarity based on above matrix by calling a function - "movie_recommendations" 
  **Step- 4:** The above mentioned function takes a movie title 'T' and returns the top 'n' movies with the highest cosine similarity based on their genres.
  **Step- 5:** Displayed the final dataframe with Top 'n' movies

**3. To develop a Collaborative based recommender system which recommends top N movies based on “K” similar users for a target user “u”**

**Function Name:** collaborative_filtering(UserID,m,k)
    - Takes 2 arguments - UserID, Number of recommendations, Threshold for similar users
    
To perform the same, I followed the below steps:

  **Step- 1:** Data was prepared with some pre-processing steps like merging different dataframe as required
  **Step- 2:** Used Pivot Table to create user-item matrix using pivot_table, where rows represent users, columns represent movie titles, and the values are ratings. Missing values (NaN) are filled with 0
  **Step- 3:** Calculated cosine similarity between users based on their movie ratings using cosine_similarity function.
  **Step- 4:** Filtered the similarity scores for the specified target user (UserID) from user_similarity_df and identified the top k most similar users (excluding the target user) based on similarity scores.
  **Step- 5:** Identified movies that the target user has rated positively (greater than 0) and movies that the top similar users have rated positively.
  **Step- 6:** Created a list of recommended items (movies) that the similar users have rated positively but the target user has not, then selected the top m recommendations from the list of recommended items
  **Step- 7:** Displayed the final dataframe recommending top 'm' movies

Additionally, I used **IPyWidgets** module to add a user-friendly UI to get the movie recommendations as per requirement.
The code output facilitates switching between different recommendation methods using tabs and input widgets.
Functions associated with button clicks extract input values, call the corresponding recommendation function, and clear the output to provide a clean display for each recommendation.

Below steps are followed for the same:

 **Step- 1:** Created Input Widgets for Popularity-Based Recommendations , Content-Based Recommendations and Collaborative Filtering:
 **Step- 2:** Created the tabs with titles "Popularity Based," "Content Based," and "Collaborative Filtering." and arranged the widgets for each tab in VBox (vertical box) and HBox (horizontal box) layouts.
  **Step- 3:** Defined functions to be called for each tab's button using on_click method
  **Step- 4:** Displayed the tabs so that User can interact with the system and get recommendations as per requirement.
