yodleeprivate
=============
The S3 bucket, **yodleeprivate**, is the home for files used by our data processing infrastructure.
it is **for internal use only** and access is restricted to Yodlee personnel and systems.

For simplicity's sake, all panel processing is grouped under the **panels** directory:
<pre>
S3://
	yodleeprivate/
		panels/
</pre>

If in the future, if we needed to support **another_type_of_processing** with S3, that directory would be placed alongside the **panels** directory:

<pre>
S3://
	yodleeprivate/
		another_type_of_processing/
		panels/
</pre>
