# Search Spider, Page Ranker and Visualizer
This is a set of programs that emulate some of the functions of a search engine.  They store their data in a SQLITE3 database named 'spider.sqlite'.
Spider:
The Spider will not re-crawl any pages already in the database.  Upon restart it goes to a random non-crawled page and starts there.  So each successive run of spider.py is additive. You can have multiple starting points in the same database - within the program these are called "webs".   The spider chooses randomly amongst all non-visited links across all the webs.
Pagerank:
Ranks all the links in the database.You can run sprank.py as many times as you like and it will simply refine the page rank the more times you run it.
For each iteration of the page rank algorithm it prints the average change per page of the page rank.   The network initially is quite unbalanced and so the individual page ranks will change wildly. But in a few short iterations, the page rank converges.  
 
Visualizer:
If you want to visualize the current top pages in terms of page rank, run spjson.py to write the pages out in JSON format to be viewed in a web browser. This shows an automatic layout of the nodes and links.  You can click and  drag any node and you can also double click on a node to find the URL that is represented by the node.
![](https://github.com/sourabh-rb/pagerank/blob/master/Pagerank%20WP.PNG )

![](https://https://github.com/sourabh-rb/pagerank/blob/master/Pagerank%20Dr.Chuck.PNG )

