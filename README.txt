# SaaS API Security Risk Analysis

This report presents the results of a read-only API Security Risk Analysis conducted on a public demo API (JSONPlaceholder). The assessment focused on identifying common API security weaknesses related to authentication, authorization, data exposure, and rate limiting. Multiple high-risk issues were identified, including unauthenticated write and delete operations, exposure of sensitive user data, and insufficient access controls. While the tested API is a demo environment, these findings represent critical risks in real-world SaaS systems and could lead to data breaches, data manipulation, service abuse, and regulatory impact if left unmitigated.

## API Testing Screenshots

The following screenshots from Postman illustrate the API endpoints tested and their security issues.

### GET /posts

![GET Posts](imagies/Postman-GET-posts.png)

This screenshot shows a GET request to retrieve all posts. The endpoint is open without authentication, allowing excessive data exposure.

![GET Posts 1](imagies/Postman-GET-posts-1.png)

Another view of the GET posts request.

### GET /posts/1/comments

![GET Comments](imagies/Postman-GET-comments.png)

GET request for comments on a specific post, exposing user email addresses without authentication.

![GET Comments 1](imagies/Postman-GET-comments-1.png)

Another screenshot of GET comments.

### POST /posts

![POST Posts](imagies/POST-posts.png)

POST request to create a new post without authentication, allowing unauthenticated write operations.

### PUT /posts/1

![PUT Posts](imagies/PUT-posts-1.png)

PUT request to update a post without authentication.

### PATCH /posts/1

![PATCH Posts](imagies/Postman-PATCH-posts-1.png)

PATCH request for partial update without authentication.

### DELETE /posts/1

![DELETE Posts](imagies/Postman-DELETE-posts-1.png)

DELETE request to remove a post without authentication.

## Report

See the full report in [report/JSONPlaceholder Test Report.pdf](report/JSONPlaceholder Test Report.pdf)
