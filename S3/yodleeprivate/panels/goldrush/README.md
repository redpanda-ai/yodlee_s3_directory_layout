goldrush_six_million
=============
The "Six million" panel is originally produced by Yodlee's GoldRush (a Hadoop based data warehouse run in a traditional data center).

Output is split into three different subfolders:
<pre>
S3://
	yodleeprivate/
		panels/
			goldrush_six_million/
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
