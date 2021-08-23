# S3

## What is Amazon S3?
- Amazon Simple Storage Service (Amazon S3) is storage for the Internet. It is designed to make web-scale computing easier.
- Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.

**Advantages of using Amazon S3**

* Creating buckets : Create and name a bucket that stores data.
* Storing data : Store an infinite amount of data in a bucket. Upload as many objects as you like into an Amazon S3 bucket.
* Downloading data : Download your data or enable others to do so.
* Permissions : Grant or deny access to others who want to upload or download data into your Amazon S3 bucket.
* Standard interfaces – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.

**Amazon S3 concepts**
*Buckets*
if the object named `photos/puppy.jpg` is stored in the `awsexamplebucket1` bucket in the US West (Oregon) Region, then it is addressable using the URL `https://awsexamplebucket1.s3.us-west-2.amazonaws.com/photos/puppy.jpg`.

*Objects*
Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata. The data portion is opaque to Amazon S3.

*Keys*
A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key. The combination of a bucket, key, and version ID uniquely identify each object.

## S3 with Amplify

To start provisioning storage resources in the backend, go to your project directory and execute the command:
     amplify add storage

Enter the following when prompted:
     ? Please select from one of the below mentioned services:
     `Content (Images, audio, video, etc.)`
     ? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
     `Yes`
     ? Do you want to use the default authentication and security configuration?
     `Default configuration`
     ? How do you want users to be able to sign in?
     `Username`
     ? Do you want to configure advanced settings?
     `No, I am done.`
     ? Please provide a friendly name for your resource that will be used to label this category in the project:
     `S3friendlyName`
     ? Please provide bucket name:
     `storagebucketname`
     ? Who should have access:
     `Auth and guest users`
     ? What kind of access do you want for Authenticated users?
     `create/update, read, delete`
     ? What kind of access do you want for Guest users?
     `create/update, read, delete`
     ? Do you want to add a Lambda Trigger for your S3 Bucket?
     `No`

To push your changes to the cloud, execute the command:  
     amplify push   

Add these libraries into the dependencies block:

     dependencies {
     implementation 'com.amplifyframework:aws-storage-s3:1.24.0'
     implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
     }