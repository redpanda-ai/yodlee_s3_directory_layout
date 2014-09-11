6m
=============
One of the panels that can be processed by the **clustering_tool**.  This system is written in Pig and runs on Elastic Map Reduce.

<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
				6m/
</pre>


This directory will have three subdirectories:
<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
				6m/
					bank/
					card/
					error/
</pre>

## bank
Each one of our daily panel files for bank transactions is kept here

## card
Each one of our daily panel files for card transactions is kept here

## error
Informative error messages for our developers can be kept here
