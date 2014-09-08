meerkat
=============
A machine-learning optimized search engine that finds the source of billions financial transactions.  Built using Python3 and ElasticSearch, in runs on the Elastic Compute Cloud.

Output is split into three different subfolders:
<pre>
S3://
	yodleeprivate/
		panels/
			meerkat/
				bank/
				card/
				error/
</pre>

## bank
Each one of our daily panel files for bank transaction is kept here

## card
Each one of our daily panel files for card transaction is kept here

## error
Informative error messages for our developers can be kept here
