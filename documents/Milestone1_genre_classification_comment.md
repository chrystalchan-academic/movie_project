# Movie genre classification

## Questions
We need to address the following problems before we do movie genre classification:
1. TMDB and IMDB have different movie genre list and this can create issues for prediction. Which list of genre we use? What do we do if they disagree?
2. A movie can have more than 1 genre. The data from TMDB and IMDB will not indicate which one is the main genre if there is more than 1 genre. However, when we do movie genre prediction, we may only want our reponse to be 1 genre. What should we predict? A genre or a list of genre?
3. If we aim to tag a movie with multiple genres, what metrics do we use to evaluate our methods?  The accuracy is no longer a simple 0-1 evaluation.

## Additional data set
Amazon API provides genre tag and frequency weighting.  We can use it to find movie primary genre.

## Approach
Below are some of our thoughts on the questions in the first section.

### TMDB genre vs IMDB genre
Issues:
	1. TMDB has a shorter genre list than IMDB list. Although we aim to pull information of the same set of movies, the genre lists extracted from IMDB and TMDB data are still different.
	2. Some genre distinction are not based on plots. For example, "Foreign" genre can refer to film out of the country.
	3. Some genre have too few movies. 
Possible solutions:
	1. We can check if the genre classification are similiar for IMDB and TMDB by the following: look at percentage breakdown of each genre. If the results are significantly different amonng the two databases, we will have to explore what causes the difference. We can then merge the list or just to use IMDB genre list if the genre are not that different from TMDB.
	2. We should perhaps remove some genres based on movie release date or country. 
	3. For genre with little movies, we can merge them into another genre. Ex. If we do cluster analysis and find Noir is indeed close to Crime, we can group movies from Noir to Crime.

### What are our reponse variable?
Issues:
	1. Movies have 3 genres on average from IMDB and TMDB.
	Unforunately, neither database tags primary genre of a movie.
Possible Solutions:
	1. We create clusteres of genres. Ex. Cluser 1 consists of Action,Drama,Romance; cluster 2 consists of Horror. A movie can be assigned to cluster 1. Some researches used this method. 
	2. We will have a outpuf vecot of Y. Y = [Y_horror, Y_romance, Y_drama,...]
	3. We can do output only 1 Y of primary genre. But to do this, we will need to get data from Amazon.
	Currently, we prefer option 2.

### Multi-label classification
We will use multi-label classification. Before we discuss which methods to use (ex. KNN, SVM), we should consdier how we will treat the response variable first.

1. Binary Relevence(BR)
we seperate each genre into seperate problems (one for each genre).
However, this ignore label dependence. 
Ex. if a movie is tagged as Drama, it is likely that it is also tagged as Action. if a movie is tagged as  Horror, it is likely that it is also tagged as Romance.
If two classes of a genre (Yes/No) have very uneven sizes in the training set, the classifier will lean toward the class with higher movie number.
There is a method called a label correction strategy that can help to improve accuracy
For example, if our prediction is [Y_horror, Y_romance, Y_drama]= [1,1,0], which does not really happen in training set. We find another likely matching vector. We may change our prediction to be [1,0,1].

2. Classifier Chains (CC)
We seperate each genre into seperate problems, but include previous predictions as predictors.
For example, X is our predictor for Y_horror. Next, X, Y_horror are our predictor for Y_romance.
However, error may be propagated down the chain.

3. Label Powerset (LP)
Instead of having seperate Y_i for each genre i, we will predict only Y. Y has 2^I possible values where I is the number of genre.
For example, if Y_horror = 1, Y_romance = 0, Y_drama = 1, Y = [101]
However, imbalance of the data can be an issue.

4. Neural network
The output node will be each genre label.

We aim to try out meothds 1 to 4 with different algorithms.
We also need to examine label dependence for each genre by examining co-occurance frequency of genre. It will give us a better picture of which method to use.
We can also transform Y to [Y_OR,Y_AND, Y_XOR].


### Classification Algorithms

Below is the list of algorithms. We will likely add more algorithms later.
1. KNN
2. Kmeans
3. Naive Bayes
4. SVM
5. LDA

### Classification Evaluation
Imagine if the reponse variable Y are Y_horror, Y_romance, Y_drama, ... for each genre i, we will need to find appropriate methods to evaluate classification methods.

We can calculate different measurements and evalute by multiple measurements.
1. Compare bit-wise
This can be too lenient
2. Compare vector-ise
This can be too strict
3. Hamming loss (for BR)
4. 0/1 loss (for CC)
5. precision 
6. recall
7. F measures

For some of the measurements above, we can use macro-average(which give equal qeight to every class) or micro-averaging(which weights class relatively to its example frequency).


