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

