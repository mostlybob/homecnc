## The Approach
Ideally, I'd like to make this relatively simple. I've reviewed a few articles on building a REST API using Go and most of them include things I don't necessarily need, yet anyway, things like a database/ORM, API frameworks and even a front end. My goal is to keep it as simple as I can. 

Since there will be an internet-facing aspect of the API, I'll need a degree of security and that's something best baked in from the start. I've seen a couple of articles mention JSON web token (JWT) for securing a front-end[^1] [^2], so I'll go with that.

Internally, I'd like to stick as close to the standard library as I can. I will `gorilla/mux` for routing, since it seems well-documented. I don't anticipate any way-out use cases. It's one of the things I like about separating the server-side API from any sort of front-end client processing - no muddying the water with code generating a web page getting mixed in with code that's doing the processing of the requests/responses. "JSON in, JSON out - that's all" seems like a nice clean approach.


[^1]: https://www.sohamkamani.com/blog/golang/2019-01-01-jwt-authentication/
[^2]: https://medium.com/@adigunhammedolalekan/build-and-deploy-a-secure-rest-api-with-go-postgresql-jwt-and-gorm-6fadf3da505b