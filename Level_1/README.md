1. What is the dataset you chose? (include a link to the dataset)

I chose a dataset containing information on concerts such as the artist, performance city, city population, music genre, 
and minimum ticket price. Here is the link:
https://github.com/ethanjaredlee/ticketmaster-price-ml/blob/master/data.csv
Note: I slightly modified the dataset to fill in a few rows that were incomplete. 
This csv is in the "Notebook(s)" folder.

2. What is the focus question you are trying to answer with this dataset? Include whether this is a classification, clustring, or other type of problem.

The focus question that I will try to answer with this data set is: 
What homogenous groups of concerts emerge based on their ticket pricing, genre, city population, and the artist's popularity?
What features influence the formation of these clusters most?

3. What is your plan for cleaning this dataset? (you don't have to go into too much detail, just a general idea of what you are going to do) 

To clean this dataset, I plan to drop rows with NaN values--for example, many rows have unknown city population sizes, so
I plan to drop these. I will also reduce the range of features of interest. For certain shows, minimum prices 
were upwards of $2000; these high prices were often taken from music festivals where the artist performed,
so they were misleading as they were not the artist's "concert." Because of this, I will remove outlier rows where the 
ticket price was above $350.00 (2 stds above the 'minprice' feature's mean).