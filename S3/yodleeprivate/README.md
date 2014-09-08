yodleeprivate
=============
The S3 bucket, **yodleeprivate**, is the home for files used by our data processing infrastructure.
it is **for internal use only** and will access is restricted to Yodlee personnel and systems.

There are currently five different modules, each within its own sub-directory.
<pre>
S3://
	yodleeprivate/
		clustering_tool/
		goldrush_six_million/
		mastercard/
		meerkat/
		pii_removed_six_million
</pre>

The following outlines the execution dependies amongst each module.
### Execution dependencies
| Execution Order | Name                    | Depends On              |
| --------------: | ----------------------- | ----------------------- |
|               1 | goldrush_six_million    | Yodlee's Data Warehouse |
|               2 | clustering_tool         | goldrush_six_million    |
|               3 | meerkat                 | clustering_tool         |
|               4 | pii_removed_six_million | meerkat                 |
|               5 | mastercard              | pii_removed_six_million |

## clustering_tool

Used to find commonly occuring permutations of our top merchants.  This system is written in Pig and runs on Elastic Map Reduce.

## goldrush_six_million

The "Six million" panel is originally produced by Yodlee's GoldRush (a Hadoop based data warehouse run in a traditional data center).

## mastercard
A subset of approximately 3 million users taken from **pii_removed_six_million**.  This is specifically for one of our customers, MasterCard.

## meerkat

A machine-learning optimized search engine that finds the source of billions financial transactions.  Built using Python3 and ElasticSearch, in runs on the Elastic Compute Cloud.

## pii_removed_six_million

Removes context-specific private information from the meerkat panels.  This system is written in Pig and runs on Elastic Map Reduce.
