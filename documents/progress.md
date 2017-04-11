## Progress
### Updates on Mar.30 - Milestone1. Part1:
1. Required package: 
    (1) "tmdbsimple", install by "pip install tmdbsimple“. More information can be found: https://github.com/celiao/tmdbsimple
    (2) "imdbpy", install by "pip install imdbpy". More inforamtion can be found: http://imdbpy.sourceforge.net/
    (3) Additional relevant API information: TMDB API: https://www.themoviedb.org/documentation/api
    (4) TMDB API KEY = "71e259894a515060876bab2a33d6bdc9"
2. Special Instructions:
    Please see the "Notes" section in the milestone1 ipython-notebook. It includes how to access movie information
    from IMDB and TMDB using different search/discover criteria.

    Since the latest TMDB movie id is 449744, API has limited access 40 requests/10 seconds, we will need around 31 hours to get all movie information. I didn't get all the movie information at my step, but I'wrote an example showing how to get movie information for TMDB id from 1 to 20 (skipped non-existing ids). At this point, we can use the methods from "Note" section to get partial movies we are interested in. After we decides what attributes are useful for the project, we can spend 31 hours to get all movies. 
###  Updates on Mar.30 - Milestone1. Part2:
1. Special Instructions:
	- I add 2 new resource on classficiation papers
	- Please load the data files instead of calling API directly for now.
	- You don't need to run any previous cells. But please run cell[1,2,3] before you start running your code. 
	- Ignore Milestone1_02_store_data_tmdb.ipynb and don't delete it. I used it to load data specically so I can still do work on the Milestone1.ipynb.
	- For IMDB, some data fields contins [personId, name] or [companyId, name]. We can extract a actor salary if we want to do data analysis on that.
	You can look at specific info we can extract from below.
https://github.com/alberanid/imdbpy/tree/master/imdb
http://imdbpy.sourceforge.net/docs/README.package.txt
	- Whenever you want to load more data, please run Milestone1_02_store_data_tmdb.ipynb then run Milestone1_02_store_data_imdb.ipynb. It is best not to run in Milestone1.ipynb so you can continue to work. 
	- Somehow we only load 1% of the data for TMDB for the id range we intended to load.
	- Also, when we load IMDB, throwing exception does not help to ignore data for invalid movid id, it will just crash.
	
###  Updates on Apr.11 - Milestone2:
1. Add load tmdb file and r code for clsutering
2. Special instructions:
please download imdb_imputed_process.csv from google drive to run the r code.