CS109B Project
=============

## Contributors

Chrystal Chan,
Yufei Gui,
Ai Xu,
Zhongzhong Xu

## Project Summary
Currently, tagging of movies' genres are still manual processes. Genres are normally assigned by experienced reviewers or critics.
Automatic genre classification can fasten the tagging process and may have higher accuracy than human suggestion.

## Requirement
Python 2.7 is used asIMDBPY does not work with Python 3.
Packages:
1. tmdbsimple
	- install by "pip install tmdbsimple“. More information can be found: https://github.com/celiao/tmdbsimple
2. imdbpy
	- install by "pip install imdbpy". More inforamtion can be found: http://imdbpy.sourceforge.net/
3. pandas
4. sklearn
5. skmultilearn


## Data
Data entry are stored in CSV format. Intermediate files are stored in google drive.
Only the finalized, cleaned files are stored in the data folder.


## Links for resources 
* [Best practice for data structure](https://www.maxmasnick.com/analysis-org/)
* [Best practice for Python](https://gist.github.com/sloria/7001839)
* [CS109 project last year](https://github.com/kennyyu/cs109-project)
* [Movie Classification Using k-Means and Hierarchical Clustering](http://sahebmotiani.com/Movie%20Clustering.pdf)
* [Movies’ Genres Classification by Synopsis](http://cs229.stanford.edu/proj2011/Ho-MoviesGenresClassificationBySynopsis.pdf)


## Folder organization
Within each folder, there is README.md file to descript more details.
Most files will be named as MilestoneX_XXXXXX to indicate which milestone it is used in.
/data: cleaned data files
/milestone_summary: pdf files submitted for each milestone
/python_notebook: python notebooks
/r: r codes



