#  Movie Recommendation System
### Authors: 
1. George Opondi
2. Jonquil Phelan
3. Vincent Kiplang'at
4. Jimmy Mumo
5. Donnah Mwaniki
6. Cynthia Gitonga
7. Brian Gikonyo
8. Ian Odhiambo


---

## Overview
The objective of this project is to build a movie recommendation system that provides personalized recommendations to users based on their ratings of other movies. The system will utilize machine learning algorithms to analyze user ratings and similarities between movies to generate a list of top 5 movie recommendations for each user.

---
## Objectives
> Develop a customized movie recommendation system using cutting-edge machine learning algorithms.

> Provide personalized movie recommendations for each user based on their preferences and viewing history.

> Enhance user experience and engagement by offering relevant and tailored movie suggestions.

---


## Business understanding

In the age of streaming services and an abundance of movie alternatives, customers frequently face the issue of finding films that match their preferences. A movie recommendation system seeks to solve this problem by using user ratings to generate individualized movie recommendations. The target audience for this project are companies that provide movie streaming services, such as Netflix, Amazon Prime Video, or Hulu, which can in turn use recommendation systems to increase their customer engagement and retention. These businesses can provide personalized movie suggestions that adapt to their audience's different preferences by employing innovative machine learning techniques and user data, resulting in growth and competitive advantage in the entertainment industry. 

---

## Data Understanding

### Source:
 a) This data set is obtained from GroupLens
 
 b) (https://grouplens.org/datasets/movielens/latest/)

### Details on the data set:

This dataset (ml-latest-small) describes 5-star rating and free-text tagging activity from MovieLens, a movie recommendation service. It contains 100836 ratings and 3683 tag applications across 9742 movies. These data were created by 610 users between March 29, 1996 and September 24, 2018. This dataset was generated on September 26, 2018.

Users were selected at random for inclusion. All selected users had rated at least 20 movies. Each user is represented by an id, and no other information is provided.

The data are contained in the following files: **links.csv**, **movies.csv**, **ratings.csv** and **tags.csv**. 

**Ratings Data File Structure (ratings.csv):** All ratings are contained in the file ratings.csv. Each line of this file after the header row represents one rating of one movie by one user, and has the following format:

userId,movieId,rating,timestamp
The lines within this file are ordered first by userId, then, within user, by movieId.

Ratings are made on a 5-star scale, with half-star increments (0.5 stars - 5.0 stars).



**Tags Data File Structure (tags.csv):** All tags are contained in the file tags.csv. Each line of this file after the header row represents one tag applied to one movie by one user, and has the following format:

userId,movieId,tag,timestamp
The lines within this file are ordered first by userId, then, within user, by movieId.


**Movies Data File Structure (movies.csv):**Movie information is contained in the file movies.csv. Each line of this file after the header row represents one movie, and has the following format:

movieId,title,genres
Movie titles are entered manually or imported from https://www.themoviedb.org/, and include the year of release in parentheses. 



**Links Data File Structure (links.csv):**Identifiers that can be used to link to other sources of movie data are contained in the file links.csv. Each line of this file after the header row represents one movie, and has the following format:

movieId,imdbId,tmdbId


### Description of columns
**User Ids:** MovieLens users were selected at random for inclusion. Their ids have been anonymized. User ids are consistent between ratings.csv and tags.csv (i.e., the same id refers to the same user across the two files).

**Movie Ids:** Only movies with at least one rating or tag are included in the dataset. Movie ids are consistent between ratings.csv, tags.csv, movies.csv, and links.csv (i.e., the same id refers to the same movie across these four data files).

**Timestamps:** represent seconds since midnight Coordinated Universal Time (UTC) of January 1, 1970.

**Tags:** are user-generated metadata about movies. Each tag is typically a single word or short phrase. The meaning, value, and purpose of a particular tag is determined by each user.

**Genres:** are a pipe-separated list, and are selected from the following:

Action, Adventure, Animation, Children's, Comedy, Crime, Documentary, Drama, Fantasy, Film-Noir, Horror, Musical, Mystery, Romance, Sci-Fi, Thriller, War, Western, (no genres listed)


### Citation
F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. https://doi.org/10.1145/2827872

---

## Visualizations

![alt text](<Images/Count of movies.png>)
Count of movies by rating

![alt text](<Images/Movie genre distribution.png>)
Movie genre by distribution

---

## Model Selection

The analysis  tested two main methods for recommending movies: SVD and KNN. SVD was more accurate than KNN, with an error rate of 0.8734 for SVD. To boost SVD's accuracy, it was  fine-tuned its settings using GridSearchCV. After tuning, SVD's accuracy improved to 0.8687, with the best settings being n_factors=50 and reg_all=0.05. Overall, SVD performed better than KNN in predicting movie ratings, especially after fine-tuning.  

---

## Making recommendations

> Integrated user ratings into the SVD model and generated personalized movie recommendations.

> Top 5 recommendations included classics like "The Godfather" and contemporary favorites like "Fight Club."

---

## Recommendations

> The movie recommendation system offers a solution to the challenge of finding personalized movie suggestions.

> Streaming platforms can leverage this system to enhance user experience, engagement, and retention.

> Recommendations for future work include enhancing the system's scalability and exploring more advanced recommendation algorithms.

---

## Conclusion

> In conclusion, this  movie recommendation system demonstrates the power of machine learning in enhancing user experience in the entertainment industry.

> Further exploration of advanced recommendation algorithms and continuous improvement of the system is required  based on user feedback and evolving preferences.

> Implementing such a system can drive customer satisfaction and loyalty, ultimately contributing to the success of streaming platforms in a highly competitive market.

