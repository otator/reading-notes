# Amazon S3

[Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites. The service aims to maximize benefits of scale and to pass those benefits on to developers.


### Amazon S3 Advantages

* **Creating buckets** – Create and name a bucket that stores data. Buckets are the fundamental containers in Amazon S3 for data storage.

* **Storing data** – Store an infinite amount of data in a bucket. Upload as many objects as you like into an Amazon S3 bucket. Each object can contain up to 5 TB of data. Each object is stored and retrieved using a unique developer-assigned key.

* **Downloading data** – Download your data or enable others to do so. Download your data anytime you like, or allow others to do the same.

* **Permissions** – Grant or deny access to others who want to upload or download data into your Amazon S3 bucket. Grant upload and download permissions to three types of users. Authentication mechanisms can help keep data secure from unauthorized access.

* **Standard interfaces** – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.

### Amazon S3 Concepts

* **Buckets**: A bucket is a container for objects stored in Amazon S3. Every object is contained in a bucket.
* **Objects**: Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata. The data portion is opaque to Amazon S3. The metadata is a set of name-value pairs that describe the object
* **Keys**: A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key. The combination of a bucket, key, and version ID uniquely identify each object.
* **Regions**: You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create. You might choose a Region to optimize latency, minimize costs, or address regulatory requirements. Objects stored in a Region never leave the Region unless you explicitly transfer them to another Region.
* **Amazon S3 data consistency model**: Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions. 


### Operations

* **Create a bucket** – Create and name your own bucket in which to store your objects.

* **Write an object** – Store data by creating or overwriting an object. When you write an object, you specify a unique key in the namespace of your bucket. This is also a good time to specify any access control you want on the object.

* **Read an object** – Read data back. You can download the data via HTTP.

* **Delete an object** – Delete some of your data.

* **List keys** – List the keys contained in one of your buckets. You can filter the key list based on a prefix.



