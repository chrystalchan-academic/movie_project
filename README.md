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
Python 2.7 is used. IMDBPY does not work with Python 3.
Packages:
    (1) "tmdbsimple", install by "pip install tmdbsimple“. More information can be found: https://github.com/celiao/tmdbsimple
    (2) "imdbpy", install by "pip install imdbpy". More inforamtion can be found: http://imdbpy.sourceforge.net/

## Data
Data entry are stored in JSON format. They are stored in google drive.
Whenever you need to run the code, get the latest copy from google drive and store in /data.
.gitignore should now exclude those JSON files.

drv_tmdb_movie_details.json store TMDB data.
drv_imdb_movie_details.json store IMDB data.

## Steps to run

## Links for resources 
* [Best practice for data structure](https://www.maxmasnick.com/analysis-org/)
* [Best practice for Python](https://gist.github.com/sloria/7001839)
* [CS109 project last year](https://github.com/kennyyu/cs109-project)
* [Movie Classification Using k-Means and Hierarchical Clustering](http://sahebmotiani.com/Movie%20Clustering.pdf)
* [Movies’ Genres Classification by Synopsis](http://cs229.stanford.edu/proj2011/Ho-MoviesGenresClassificationBySynopsis.pdf)


## Instructions (For team member, please read):
1. Git
	- Always pull latest master branch
	- start a new branch from a master whenever you work on, it will be best to avoid to work on master branch first. 
	- After your code is done, you can merge with master branch.
2. Folder organization
	- It will be useful to follow the practice in "Best pracice for data structure". But we can keep it simple by at least storing in an organized structure.
	- /data: data files
	- /documents: any relevent answers to question asked in project guideline, photos of sketches to visualizations
	- /python_notebook: python notebook - There should be only 1 python notebook per milestone.
	- /r: r code if there is any
	- feel free to add folders if seems apprpriate
3. README.md
	- Please update the README file on or any package we have to install.
	- if you see any useful resources, add into "Links for resources ". 
4. Coding practice
	- we don't have to comment everything, but if the section you write seems complicated, please add some comment.
	- It will be useful to follow the practice in "Best pracice for Python", you can look at only Naming section. The most important part is keep the variable naming convention consistuent.
5. documents/progress.md
	- Plesae update this for comment on what you did for this commit
	- This is used for communication within team
6. documents/task.md
	- divid up task for each member
6. Feel free to add any other suggestion~~


