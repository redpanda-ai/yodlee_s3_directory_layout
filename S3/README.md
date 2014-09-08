S3
==============
All of our work will reside in one of two buckets, either **yodleeprivate** or **yodleeproducts**.
Anything currently placed outside of these two buckets **MUST BE MOVED** as soon as this document is ratified.

<pre>
S3://
	yodleeprivate/
	yodleeproducts/
</pre>

## yodleeprivate
The S3 bucket, **yodleeprivate**, is the home for files used by our data processing infrastructure.
it is **for internal use only** and will access is restricted to Yodlee personnel and systems.
YSO and Operations heavily regulate access to this bucket, and access is only available from certain whitelisted IP addresses.
All documents written here must use Server Side Encryption / AES-256 (this is enforced by the S3 bucket policy).

<pre>
S3://
	yodleeprivate/
</pre>

## yodleeproducts
The S3 bucket, **yodleeproducts**, is the home for every data product we provide to our customers via S3.
it is **public-facing** but access is restricted to certain AWS and IAM users, to restrict customer access.

<pre>
S3://
	yodleeproducts/
</pre>


