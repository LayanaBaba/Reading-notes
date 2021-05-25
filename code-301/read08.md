## API Design Best Practices

**What does REST stand for?**

REST an architectural approach to designing web services. REST is an architectural style for building distributed systems based on hypermedia. 

**REST APIs are designed around a** resources.

**What is an identifer of a resource? Give an example.**

is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be: https://adventure-works.com/orders/1

**What are the most common HTTP verbs?**

The most common operations are GET, POST, PUT, PATCH, and DELETE.

**What should the URIs be based on?**

Resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

**Give an example of a good URI.**

https://adventure-works.com/orders 

**What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

Chatty web API is that all web requests impose a load on the web server. The more requests, the bigger the load. 

**What status code does a successful GET request return?**

A successful GET method typically returns HTTP status code 200 (OK). 

**What status code does an unsuccessful GET request return?**

If the resource cannot be found, the method should return 404 (Not Found).

**What status code does a successful POST request return?**

If a POST method creates a new resource, it returns HTTP status code 201 (Created

**What status code does a successful DELETE request return?**

If the delete operation is successful, the web server should respond with HTTP status code 204.

