pii_removed_six_million
=============
Removes context-specific private information from the meerkat panels.  This system is written in Pig and runs on Elastic Map Reduce.

Output is split into three different subfolders:
<pre>
S3://
	yodleeprivate/
		panels/
			pii_removed_six_million/
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
