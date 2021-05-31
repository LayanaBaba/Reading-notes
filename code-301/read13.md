## Status Codes Based On REST Methods

**In your own words, describe what each group of status code represents:**

* 100’s = These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.

* 200’s = These are the success codes.

* 300’s = These are redirection codes. 

* 400’s = These are the client error codes. 

* 500’s = These are the server error codes. 


**What is a status code 202?**

This doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.


**What is a status code 308?**

This tells the client to use another URL to access the resource and not use the current URL anymore.

**What code would you use if an update didn’t return data to a client?**

* 200 OK.

* 204 No Content.

* 202 Accepted. 

**What code would you use if a resource used to exist but no longer does?**

410 Gone.

**What is the ‘Forbidden’ status code?**

403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.


## Build A REST API With Node.js, Express, & MongoDB - Quick

**Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

Because it have a sensitive information.

**What is middleware?**

Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system.

**What does app.use(express.json()) do?**

express.json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. This method is called as a middleware in your application using the code: app.use(express.json());

**What does the /:id mean in a route?**

This means the component will see the dynamic part in the id parameter.

**What is the difference beween PUT and PATCH?**

PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PATCH is used when you want to apply a partial update to the resource.

**How do you make a defalut value in a schema?**

Your schemas can define default values for certain paths. If you create a new document without that path set, the default will kick in.

**What does a 500 error status code mean?**

Internal Server Error.

**What is the difference between a status 200 and a status 201?**

* 200 - OK : The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed.

* 201 - Created : A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).