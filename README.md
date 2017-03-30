CS109B Project
=============

## Contributors

Chrystal Chan
Yufei Gui
Ai Xu
Zhongzhong Xu

## Project Summary

## Package Dependecy

## Steps to run

## Links for resources 
* [Best practice for data structure](https://www.maxmasnick.com/analysis-org/)
* [Best practice for Python](https://gist.github.com/sloria/7001839)
* [CS109 project last year](https://github.com/kennyyu/cs109-project)

### For team member, please read:
## Instructions
1. Git
	- Always pull latest master branch
	- start a new branch from a master whenever you work on, it will be best to avoid to work on master branch first. 
	- After your code is done, you can merge with master branch.
2. Folder organization
	- It will be useful to follow the practice in "Best pracice for data structure". But we can keep it simple by at least storing in an organized structure.
	- /data: data files 
	- /documents: any relevent answers to question asked in project guideline, photos of sketches to visualizations
	- /python_notebook: python notebook
	- /r: r code if there is any
	- feel free to add folders if seems apprpriate
3. README.md
	- Please update the README file on how to run your code or any package we have to install.
	- if you see any useful resources, add into "Links for resources ". 
4. Coding practice
	- we don't have to comment everything, but if the section you write seems complicated, please add some comment.
	- It will be useful to follow the practice in "Best pracice for Python", you can look at only Naming section. The most important part is keep the variable naming convention consistuent.
5. Feel free to add any other suggestion~~


Updates on Mar.30 - Milestone1. Part1:
1. Required package: 
    (1) "tmdbsimple", install by "pip install tmdbsimple“. More information can be found: https://github.com/celiao/tmdbsimple
    (2) "imdbpy", install by "pip install imdbpy". More inforamtion can be found: http://imdbpy.sourceforge.net/
    (3) Additional relevant API information: TMDB API: https://www.themoviedb.org/documentation/api
    (4) TMDB API KEY = "71e259894a515060876bab2a33d6bdc9"
2. Special Instructions:
    Please see the "Notes" section in the milestone1 ipython-notebook. It includes how to access movie information
    from IMDB and TMDB using different search/discover criteria.

    Since the latest TMDB movie id is 449744, API has limited access 40 requests/10 seconds, we will need around 31 hours to get all movie information. I didn't get all the movie information at my step, but I'wrote an example showing how to get movie information for TMDB id from 1 to 20 (skipped non-existing ids). At this point, we can use the methods from "Note" section to get partial movies we are interested in. After we decides what attributes are useful for the project, we can spend 31 hours to get all movies. 



