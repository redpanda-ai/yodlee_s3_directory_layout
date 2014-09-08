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
| Name                    | Depends On              | Execution Order |
| ----------------------- | ----------------------- | --------------: |
| clustering_tool         | goldrush_six_million    | 2               |
| goldrush_six_million    | Yodlee's Data Warehouse | 1               |
| mastercard              | pii_removed_six_million | 5               |
| meerkat                 | clustering_tool         | 3               |
| pii_removed_six_million | meerkat                 | 4               |


