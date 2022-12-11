# WHY-NOT-Questions-Explanation-After-Movie-recommedation

In this work, we focus on explanations for items that do not appear in the recommendations they waywe expect them to, expressed in why-not questions, to aid the system
engineer improve the recommender. That is, instead of offering explanations on every item proposed by the system, we allow the developer give feedback about items that were not proposed. We consider here the most
traditional category of recommenders, i.e., the collaborative filtering.

We propose to characterise why-not questions by three main properties:
(i) their level of absenteeism,  (E.g Why not Titanic movie is recommended?)
(ii) their granularity  (Why not rank Titanic first?)
(iii) their dependency to existing recommended items (E.g Why there are not any comedy movies but there are horror movies?)


(Total Absenteeism, Atomic Granularity)
Why not "The Abyss (1989) "?

Inputs will be movie lens dataset, rating scores, group recommendation list, Most similar peers (Top 10) of each three group members, similar peers watched movies and ratings.

1) Check if the req. movie is in the data base of movie lens.
-If no, explanation (“Movie is not in the data base).

2) Check if the movie is in the list of rec. movies.
       - If No, explanation would be (“Not available in the data base of rec. list").
 Peers of group users have not rated this movie as common.


3) Check, if movie appears in first 40 rec. entries of movies.
           If not, “Movie group rating is less than the threshold rating of 	4.10 to be in top 40 movies”

4) Whether all Group User has been received recommended 	rating_score for the movie.
            If Not, “Explanation” Not all the members received group 	recommendation, which has reduced the average movie 	recommendation score”
           For a group user which has not received movie rating, 
           Explanation “ Most similar peers of this group user have not rated or dislikes the movie”
           
           
4.2 If all three group members has atleast got recommended 	score for this movie. 
Now check which user has caused the low avg_score of recommendation list. 
    Find the 2 group member min. rec_score with in the 3 group users.

4.3 Now check Most Similar Peers of those group users only.
Get mean rating of these 2 group Users' Most Similar peers.
If, The mean rating of Most Similar Peers of group user is lower < threshold 4.00.
Explanation “Most Similar Peers of group users donot likes  the movie.
Or “X of Most similar Peers for the group user donot likes movies.



(Granularity: Group Cases)
 - Why not "Comedies"?
1) Check ,If there is any ONLY COMEDY GENRE in the top 20 group    recommendation list.

2) 2) Since there is no ONLY COMEDY GENRE in top 20, we will then look into the remaining list.
“It means no Most similar peers of group users have highly rated a similar COMEDY GENRE movie”
If whole recommendation list is empty of COMEDY, then “no peers of group users have watched and rated similar movies.”
Or it means peers of group users do not likes Comedy much 

 3) COMEDY GENRE is in the recommendation list, but not in top 20.
now reason of why not being in top 20
     - top 20 movies rating must be more than 4.5
     - top 40 movies rating must be more than 4.10
only one movie in top 50
we will find reason of COMEDY being low ranked. 
      a)  group users' peers have not rated highly the same Comedy 	movies
      b)Peers of group users dislike movies

Check group users recommendation list.
If group users have less than 25% of the Genre in top 20,
We consider it that peers of group user donot like watch COMEDY GENRE much

Check group user recommendations, what scores they have received for Comedy movies only
If group users have less than 25% of the Genre in top 20,
we consider it that peers of group user donot like watch COMEDY GENRE much.



Position Absenteeism:
Why not "Sixth Sense, The (1999)" first?

- Check Each group user recommended movie score for the movie: Sixth Sense, The (1999)
- 1 we will compare the "Sixth Sense, The" movie with the first movie in the group  recommendation list
- Check Most Similar peers of group user: 2, most similar Peers ratings for the target movie: The Six Sense
- Check which group users have received low rec. score for the movie “Sixth Sense”
- Check Most Similar peers of group user: 2, most similar Peers ratings for the top rec group movie: Reservoir Dogs
- 




