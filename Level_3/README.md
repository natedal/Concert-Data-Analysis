- What evaluation metrics did you choose to use?

I chose to use the Silhouette Coefficient to evaluate the effectiveness of my model. 
The Silhouette Coefficient measures within-cluster similarity and between-cluster dissimilarity, which is useful for my goal
of establishing set groups of concerts without labels.

- What was the score you got for each of these metrics?

After tweaking the parameters of my DBSCAN model, I attained a silhouette score of .52.
This means that concerts within the same clusters are closer to each other in Euclidean space than they are to
concerts outside their cluster. Formation of concert clusters was influenced most strongly by features such as 
city population and genre. The silhouette score of .52 represents that concerts in cities of similar population sizes 
and similar genre tend to form distinct groupings of concerts.

Using the model parameters recommended by my silhouette score, I evaluated my model using the Davies-Bouldin Index
and attained a score of 11.8. This further indicates that the concert clusters have low within-cluster variation 
and high separation from other clusters.

Since the silhouette score is closer to 1 and the DBI is closer to 0, this indicates that my clusters are generally well-separated
in the context of the dataset. Thus, my selected features (city population, genre, minimum ticket prices, and artist popularity)
give rise to distinct groups of concerts.

- Mention any resources you used to help you in this portion of the challenge (we love links!).

To learn about evaluation metrics for unsupervised clustering, I used this article:
https://towardsdatascience.com/7-evaluation-metrics-for-clustering-algorithms-bdc537ff54d2?gi=5d3f96e24528

I used these articles to learn more about how a Silhouette Score is computed:
https://towardsdatascience.com/performance-metrics-in-machine-learning-part-3-clustering-d69550662dc6
https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html

Finally, I used this article to learn which metrics are most suitable for density based clustering algorithms.
https://www.geeksforgeeks.org/dbscan-clustering-in-ml-density-based-clustering/

- Any extra information you'd like to include

Related to the above point, I had a hard time finding intrinsic evaluation metrics that are suitable to density based clustering algorithms.
Intrinsic measures such as the silhouette coefficient interpret noise as a separate data cluster, which leads to lower scores for density based algorithms
compared to algorithms such as KMeans, which generate spherical, well-separated clusters.