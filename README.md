Google Webmaster Tools Search Referral Analysis
===============================================

This code analyzes search referral data from Google Webmaster Tools.

To run the analysis on your site, first download a data set of search data:

1. Go to "Traffic > Search Queries" (for example https://www.google.com/webmasters/tools/top-search-queries?siteUrl=http%3A%2F%2Fwww.example.com%2F)
2. Select a date range
3. Select "Show [500] rows"
4. In the URL, replace "grid.s=500" with "grid.s=10000" (or some very large number)
5. Click "Download this table" to download the CSV file.

Then, define the branded keywords for your site in `run_keyword_analysis.py`.
You need to modify the regular expression `re_branded`.

Finally, run `python run_keyword_analysis.py -c CSVFILE -o OUTPUT_DIRECTORY`
to run the analysis.  This writes a few plots plus a list of all branded
keywords to the output directory.



Dependencies
============

This was developed in Python 2.6/7 and built on top of `numpy` and `matplotlib`.


