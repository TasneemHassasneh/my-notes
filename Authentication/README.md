# Authentication

## Securing Passwords

When it comes to securely storing passwords, one commonly used technique is *hashing*. **Hashing is a process that takes a password and transforms it into a fixed-length string of characters, called a hash.** The important thing about hashing is that it is a **one-way process, meaning it is computationally infeasible to reverse the process and obtain the original password from the hash.**

To safely hash and store a password, we can use a cryptographic algorithm specifically designed for password hashing, such as *Bcrypt*. **Bcrypt is a popular and widely trusted algorithm that incorporates several security measures to protect passwords.**

When storing a password using Bcrypt, here's how the process typically works:

1. Generate a random salt

2. Hash the password

3. Store the hashed password

4. Verify passwords

Now, let's address why we would use something like Bcrypt. Here are a few reasons:

1. Security

2. Salting

3. Adaptive hashing

4. Trusted and widely used

By using Bcrypt or similar secure hashing algorithms, we can significantly enhance the security of stored passwords and protect user accounts from unauthorized access, even if the database or storage system is compromised.

---

## Basic Auth

Basic Authentication **is a simple authentication scheme used in HTTP (Hypertext Transfer Protocol) to authenticate a user's credentials when accessing a protected resource. It involves including the username and password in the HTTP headers of a request.**

In Basic Authentication, the client (typically a web browser or an HTTP client) encodes the username and password and includes them in the "Authorization" header of the HTTP request. The server then validates the credentials and grants access to the requested resource if they are correct.

The properties necessary in the header of a Basic Auth request are as follows:

1. Authorization Header: The "Authorization" header is used to carry the authentication credentials. It has the following format:
  
   ``` javascript
   Authorization: Basic <credentials>
   ```

2. Credentials: The `<credentials>` part of the Authorization header contains the encoded username and password. It consists of the word "Basic" followed by a space and the Base64-encoded string of the username and password.

To encode the username and password in Basic Authentication, the following steps are taken:

1. Concatenation: Concatenate the username and password with a colon (":") separator. For example, if the username is "john" and the password is "password123", the concatenated string would be "john:password123".

2. Base64 Encoding: Encode the concatenated string using Base64 encoding. The resulting encoded string is what is included in the Authorization header. In our example, the Base64-encoded string for "john:password123" would be "am9objpwYXNzd29yZDEyMw==".

---

## OWASP auth cheatsheet

Authentication **is the process of verifying the identity of a user or entity to ensure they are who they claim to be.** In the context of a web application, **it is the mechanism that allows users to access certain resources or perform specific actions based on their authenticated identity.**

Here's a simplified explanation of the *authentication process* for a non-technical recruiter:

1. User Identification: The user provides their username or email address to indicate their identity.

2. Password Submission: The user submits their password, which is a secret, known only to them, to prove their authenticity.

3. Server-side Validation: The server receives the username and password and validates them against the stored credentials. If the credentials match, the server proceeds with authentication.

4. Authentication Result: If the credentials are valid, the server generates a session or authentication token, which represents the authenticated user. This token is then sent back to the user's browser or client.

5. Accessing Protected Resources: For subsequent requests to protected resources, the user includes the authentication token in the request header. The server verifies the token and grants access if it is valid and not expired.

Regarding error messaging, it is crucial to handle authentication errors properly to maintain security and provide a user-friendly experience:

1. HTTP Error Codes: When an authentication error occurs, appropriate HTTP status codes should be returned to the client. For example, a status code of 401 (Unauthorized) can be used when the user's credentials are invalid or missing, and 403 (Forbidden) can be used when the user does not have sufficient privileges to access a resource. These status codes provide meaningful information to the client about the nature of the error.

2. HTML Error Messages: Along with the HTTP status code, it is essential to provide informative and user-friendly error messages to the user. These messages should not disclose specific details about the error to prevent potential security risks. Instead, they should provide general guidance or instructions on how to resolve the issue. For example, a message like "Invalid username or password" can be displayed when authentication fails.

By bookmarking the OWASP (Open Web Application Security Project) fundamentals and considering them during authentication implementation, you can ensure that your application follows secure practices. OWASP provides valuable resources and guidelines for building secure applications and helps identify and mitigate common security vulnerabilities.

Developing applications with security in mind from the beginning reduces the likelihood of vulnerabilities throughout the application's lifecycle. It's essential to stay informed about current security best practices and regularly update and review your application's security measures to ensure the ongoing protection of user data and resources.
