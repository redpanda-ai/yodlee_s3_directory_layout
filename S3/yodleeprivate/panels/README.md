panels
=============
<pre>
S3://
	yodleeprivate/
		panels/
</pre>

The **panels** directory hosts our data panel processing infrastructure.
Different working areas, or **modules**, each have their own sub-directory for a different type of work.
There are currently five modules:
<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
			goldrush_six_million/
			cmc_panel/
			meerkat/
			pii_removed_six_million
</pre>

The following outlines the execution dependies amongst each module.
### Execution dependencies
| Execution Order | Name                    | Depends On                                 |
| --------------: | ----------------------- | ------------------------------------------ |
|               1 | goldrush_six_million    | Yodlee's Data Warehouse                    |
|               2 | clustering_tool         | any panel, such as goldrush_six_million    |
|               3 | meerkat                 | clustering_tool                            |
|               4 | pii_removed_six_million | meerkat                                    |
|               5 | cmc_panel              | pii_removed_six_million                     |

## clustering_tool

Used to find commonly occuring permutations of our top merchants.  This system is written in Pig and runs on Elastic Map Reduce.

## goldrush_six_million

The "Six million" panel is originally produced by Yodlee's GoldRush (a Hadoop based data warehouse run in a traditional data center).

## cmc_panel
A subset of approximately 3 million users taken from **pii_removed_six_million**.  This is specifically for one of our customers.

## meerkat

A machine-learning optimized search engine that finds the source of billions financial transactions.  Built using Python3 and ElasticSearch, in runs on the Elastic Compute Cloud.

## pii_removed_six_million

Removes context-specific private information from the meerkat panels.  This system is written in Pig and runs on Elastic Map Reduce.

