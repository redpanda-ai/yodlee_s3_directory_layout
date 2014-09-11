clustering_tool
=============
Used to find commonly occuring permutations of our top merchants.  This system is written in Pig and runs on Elastic Map Reduce.

Output is organized by the name of the panel the cluastering_tool has been run on:
<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
				6m/
</pre>

The clustering tool can be used on a variety of panels, so if we wanted to add **some_other_panel**, it would be placed alongside **6m** in its own directory:

<pre>
S3://
	yodleeprivate/
		panels/
			clustering_tool/
				6m/
				some_other_panel
</pre>
