CS109B Project
=============

## Data
whole_data.zip contains whole_data.csv and whole_data_y.csv
whole_data.csv 
- it is the cleaned file with only features from IMDB used for predictions.
- it contains genre as column of binary variable. Ex. if a movie's IMDB genre contains "Horror", the column "Horrow" will be 1, else 0.
- it contains clusters as column of binary variable. Ex. if a movie's IMDB genre is in cluster 1,  the column "Cluster1" will be 1, else 0.
whole_data_y.csv
- it is used for milestone5 deep learning. Due to computational power limit, we have to model the problem as multi-classs in milestone5 instead of mult-class in milestone 1- 4, we creat another file that categorize the movie by the closest cluster. y will be [1,7].