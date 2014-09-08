clustering_tool
=============
Used to find commonly occuring permutations of our top merchants.  This system is written in Pig and runs on Elastic Map Reduce.

Output is split into three different subfolders:
<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
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
