/r/wallstreetsbets scraper for live data.

This uses beta.pushshift.io to grab comments between 10 and 20 minutes old (plus or minus some seconds depending on the scheduler) with 1 or more points from /r/wallstreetbets. The comments are run through a word parser to look for stock tickers. Those comments are also run through vaderSentiment (created by CJ Hutto and then further editted by Ryan Elliot) to give them a "sentiment score." All of this is sent to a mongoDB database to eventually be pulled and displayed on wsb-data.vercel.app.
