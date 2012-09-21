testing
=======




The module is used to find sites that are discussing ActiveState, its technologies, competitors or other things of interest to ActiveState on a regular basis.

The ActivesState alert module preforms  a series of searches using APIs provided by Google and Twitter. Results are cached, deduplicated and formatted in a nice e-mail to specified recipients. 


Features:
* Preforms searches against:
  * Google
    * News
    * Blogs
    * Video
    * Images (Implemented but not used)
 * Twitter
* Has one or more projects
* Each Projects specifies
  * Title and descriptions
  * E-mail recipients
  * One or more categories, each one specifies
    * A section title
    * A list of search expressions to send to the specified API. Example  containg "komodo and activestate" but not "komodo and comic con"
    * Content, that if found in the "Hit" will exclude the hit from being returned

* Content is ignored if
  * It is older than 24 hours. The age of content is determined by subtracting the time that the content was posted online versus the time it was returned in the search

 * It is from a url that is hosted on activestate.com or sys-con.com domains

 * One e-mail for each project along with all the results for the given categories is sent

* Each  e-mail is formatted  for both Text and HTML

* The content of the e-mail along with the cache of URLS seen  are stored in SVN
  
  