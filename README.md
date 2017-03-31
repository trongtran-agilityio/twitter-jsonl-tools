## twitter-jsonl-tools

Simple set of Python tools for handling Twitter data in the *JSONL* (JSON Lines text) format, also called newline-delimited JSON. See [http://jsonlines.org](http://jsonlines.org) for more details on the format.

### Dependencies
Tested with Python 3.6, and requiring the following packages, which are available via PIP:

* [prettytable >= 0.7.2](https://code.google.com/p/prettytable/)

### Basic Usage - Tweets

The tools used to process tweets expect one or more JSONL files as inputs, where each line contains a JSON-formatted tweet as retrieved from the Twitter API.

To get basic summary statistics for a JSONL file containing tweets:

	python jsonl-tweet-stats.py sample/sample-tweets-500.jsonl

To get list of the most frequently-tweeting users for a JSONL file containing tweets:

	python jsonl-tweet-authors.py sample/sample-tweets-500.jsonl 

To get list of the most frequently-mentioned users for a JSONL file containing tweets:

	python jsonl-tweet-mentions.py sample/sample-tweets-500.jsonl 

To get list of the most frequently-appearing hashtags for a JSONL file containing tweets:

	python jsonl-tweet-hashtags.py sample/sample-tweets-500.jsonl

To export all tweets in a simple CSV (comma-separated) format:
	
	python jsonl-tweet-export.py sample/sample-tweets-500.jsonl -o sample/sample-tweets.csv
