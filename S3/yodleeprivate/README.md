yodleeprivate
=============
The S3 bucket, **yodleeprivate**, is the home for files used by our data processing infrastructure.
it is **for internal use only** and will access is restricted to Yodlee personnel and systems.
YSO and Operations heavily regulate access to this bucket, and access is only available from certain whitelisted IP addresses.
All documents written here must use Server Side Encryption / AES-256 (this is enforced by the S3 bucket policy).

<pre>
S3://
	yodleeprivate/
</pre>

<pre>
S3://
	yodleeprivate/
		clustering_tool/
		goldrush_six_million/
		mastercard/
		meerkat/
		pii_removed_six_million
</pre>

### Sequence
| Name                 |Input Source             | Depends On             |
| -------------------- | --------------------    | ---------------------- |
| clustering_tool      | goldrush_six_million    | goldrush_six_million   |
| goldrush_six_million | Yodlee's Data Warehouse | Yodlee's Data Warehouse|



