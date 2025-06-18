```
To provide authentication over microservices, we would need to implement any one of the below solutions.

1. Redis session storage
2. Implement JWT authentication for all the services, we can provide a auth token during auth and that can be stored in cookie.
3. Use an api gateway, that will act like load balancer to other services.
```