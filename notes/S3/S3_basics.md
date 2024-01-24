# Simple Storage Service | S3

Amazon S3 is a **global** storage system for the internet, designed to ***work in high scale***, through a *simple interface* of web services.

It's used to storage and/or retrieve any amount of data, at any moment, from anywhere in the web.

Some Amazon S3 advantages are:
- Buckets creation
- Data storage
- Data download
- Permissions
- Default interface

## Some more basic concepts

### *Buckets:*  
- It's a container for objects stored in Amazon S3, where each objects is in a bucket.

- Each buckets should have a ***global unique name***.
    - It **should** have between 3 and 63 characters
    - **Should** have only lowercase letters, number, dots and hyphens
    - **Should** start and end with a letter
    - **Shouldn't** be an IP address

- Even though a S3 is a global resource, a ***bucket is a regional resource***.

- The **maximum size** of a bucket is *5TB*

- A bucket example is like this:
    - ***s3://my-bucket-s3*** — This is for CLI usage

    - ***https://my-bucket-s3.s3.amazon.com/*** — This is for browser access

---

### *Objects:*
- Objects are the fundamental entity (data) stored on Amazon S3.

- Objects are made of metadatas and object data.

- The identification of an object is composed by the combination of ***a bucket, a key, and a version ID.***

- Each *object* is addressed exlusively by the ***combination* of the web service endpoint, bucket name, it's key and optionally it's version**.

- Objects larger than 5GB to be sent **necessarily should** use ***Multi-part Upload***.
    - Amazon recommends that even **objects 100MB in size** should use *Multi-part Upload* for a faster data transfer.

---

### *Keys:*
- It's an unique bucket identifier.

- Each object in a bucket has **only one key**.

- Each key is composed by an **prefix** and a **object name**.
    > https://**docs**.s3.amazonaws.com/**2024-01-01/textfile.txt**

---

### *Regions:*
- You can choose in which region a Bucket should be created.

- The decision can be based on latency optimization, lowering costs or to attend any regulatory requirements.

- Objects in a region ***NEVER*** leave it.