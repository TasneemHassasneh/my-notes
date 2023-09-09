## Review API Server Build

An API (Application Programming Interface) server is a fundamental component of web applications that allows different software systems to communicate with each other. It typically handles incoming requests, processes them, and sends back responses. Building an API server involves creating endpoints that define how clients (like web or mobile apps) can interact with your application.

## Query String Parameter vs. Path Parameter

1. Query String Parameter:

    * Query string parameters are typically appended to the end of the URL after a question mark (?).
They are used to provide additional data or options to an API endpoint.
Example: http://our-site.com/api/v3/stuff?param1=value1&param2=value2
Query string parameters are often optional and can be used for filtering, sorting, or customizing the response.

2. Path Parameter:

    * Path parameters are part of the URL's path and are used to specify a variable value within the URL structure.
They are often used to identify a specific resource or object.
Example: http://our-site.com/api/v3/stuff/things
Path parameters are typically required and used for resource identification.
API URL with a Path ID Parameter

## Given the provided information:

* Domain: http://our-site.com
* Version: v3
* Model name: stuff
* ID: things

*The API URL with a path ID parameter for accessing the **things** resource might look like this:
**http://our-site.com/api/v3/stuff/things***

## Dynamic API with an "Interface" to a Non-Technical Friend

Imagine the interface of our API like the menu at a restaurant. You know how you look at the menu to see all the dishes they serve? In the same way, our API has an interface that lists all the different things you can ask it to do. Each item on the menu (or in the API interface) represents a different task or piece of information you can request. So, just like you order food from the menu, you send requests to the API interface to get the data or perform actions you need for your app. It's like a friendly waiter taking your order and bringing you what you asked for.

## Review Auth Server Build

*An authentication (Auth) server* is responsible for verifying the identity of users or applications trying to access a system. It ensures that only authorized individuals or services can use the resources and services provided.

## Using Middleware for Basic and Bearer Auth

1. Basic Auth: 
    * Middleware can be used to implement Basic Authentication by checking the username and password provided in the request headers. If they match the expected credentials, access is granted.

2. Bearer Auth: 
    * Middleware can also implement Bearer Authentication by examining the token provided in the request headers. If the token is valid, it allows access.

## OAuth Handshake

OAuth is like a secret handshake between your app and another service, like when you and your friend have a special way to greet each other. In OAuth, your app needs to prove it's allowed to access someone else's data. So, it sends a request with a secret code to the other service. If the code is right, the service gives your app a special key to use whenever it needs data. It's like your friend recognizing your secret handshake and letting you into their clubhouse.

## Role-Based Access Control (RBAC) for a Non-Technical Friend

RBAC is like a backstage pass at a concert. Imagine there's a concert with different areas - the stage, the dressing rooms, and the audience area. RBAC assigns roles to people, like "performer," "crew member," and "audience." Each role has its own pass, which lets you go to certain areas. Performers can access the stage, crew members can go backstage, and the audience stays in their area. It's a way to make sure everyone only goes where they're supposed to, just like having the right pass at a concert.