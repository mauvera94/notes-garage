---
title: Non-Technical Dictionary of API Error Responses
created: 2025-02-5
updated: 2025-02-05
description: 
aliases: 
---
### 400 - Bad Request

The request was incorrect or missing something, so the server couldn’t understand it. Example: Submitting a form with incomplete or invalid data.

### 401 - Unauthorized

The request is missing proper authentication. Example: Trying to access an account without logging in.

### 403 - Forbidden

You’re authenticated but don’t have permission to access this resource. Example: Trying to open a document that you don’t have access to.

### 404 - Not Found

The requested resource doesn’t exist. Example: Clicking a broken link or mistyping a URL.

### 500 - Internal Server Error

Something went wrong on the server’s side, but it’s not your fault. Example: The system crashes unexpectedly.

### 501 - Not Implemented

The server doesn’t support the requested action. Example: Trying to use a feature that hasn’t been built yet.

### 502 - Bad Gateway

The server acting as a middleman (gateway) got an invalid response from another server. Example: A temporary issue when a service provider is down.

### 503 - Service Unavailable

The server is temporarily unable to handle the request, often due to high traffic or maintenance. Example: A website is overloaded with visitors.

### 504 - Gateway Timeout

The server acting as a middleman (gateway) took too long to get a response from another server. Example: A slow network causing a timeout.

---
## References
- [HTTP response status codes - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#client_error_responses)