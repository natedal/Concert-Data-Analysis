- What is your plan for creating this model? (you don't have to go into too much detail, just a general idea of what you are going to do) 

To create my model, I am going to perform Principal Component Analysis on my data to represent it in fewer dimensions. 
I will perform PCA on the "population," "minimum price", "genre", and "popularity score" features of my dataset, as I suspect these 
features will be the most interrelated in determining distinct clusters (lower population = higher prices, pop, rock and rap genres 
= higher prices and higher artist popularity, etc). I will use the resulting PCA scores as features for my DBSCAN algorithm. 

- Describe the algorithm that you chose and include why you think it is best suited for your problem.

To create a model that clusters concerts into separate groups, I chose to use SKLearn's DBSCAN algorithm. Due to factors such as 
overpriced shows at music festivals and at small venues (popular artist at a smaller venue = higher prices), outliers and noise are common in the dataset I selected. 
Because of this, I decided that an algorithm which "defines" clusters as circular and uniform (such as KMeans) would not be effective. 
I also had no prior knowledge of whether my clusters would be of similar size, and assumed that some clusters would be densely
packed while others would be sparsely populated, as certain popular artists had ticket prices that were much higher than the average.

- Mention any resources you used to help you in this portion of the challenge (we love links!).

To learn about DBSCAN and PCA, I used these videos from StatQuest: 
https://www.youtube.com/watch?v=RDZUdRSDOok
https://www.youtube.com/watch?v=RDZUdRSDOok

I used this article to learn about implementing PCA in python and using PCA scores to train an sklearn model:
https://365datascience.com/tutorials/python-tutorials/pca-k-means/

Finally, I used this article to understand how to visualize my data using PCA components as axes:
https://plotly.com/python/pca-visualization/