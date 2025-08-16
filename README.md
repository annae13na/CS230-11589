# CS 230 – Module Eight Journal: Portfolio Reflection  
**Author:** Anna Fuentes  
**Course:** CS230-11589 – Operating Platforms 2025  
**Institution:** Southern New Hampshire University  

---

## Reflection

### Client and Software Requirements  
The Gaming Room is a company that wanted to expand its Android game *Draw It or Lose It* into a web-based, cross-platform version. The software needed to support multiple teams and players, ensure that names were unique, and use only one instance of the game service in memory through the Singleton pattern. The client also wanted the game to be scalable, secure, and able to run smoothly across different devices.  

### What I Did Well  
I did well in creating a clear design structure that matched the client’s needs. I built a domain model that used inheritance and encapsulation to avoid duplicate code, and I applied design patterns such as Singleton and Iterator to keep the system efficient. I also feel confident about my platform recommendations, such as choosing Ubuntu Server LTS and PostgreSQL, because they balance cost, reliability, and scalability (Ubuntu, n.d.-a; Ubuntu, n.d.-b; Oracle, n.d.).  

### How the Design Document Helped the Code  
Writing the design document first really helped when it came time to think about coding. It made me slow down and plan instead of just jumping in. By laying out factors such as memory management, storage, and system layers, I already had answers to a lot of problems before I started building. For example, knowing I would use REST APIs and possibly WebSockets gave me a roadmap for how communication would work between players (Mozilla, n.d.; IETF, 2011; PostgreSQL, n.d.).  

### What I Would Revise (and How)  
If I could revise one part of my design document, I would add more detail to the security section. I mentioned features such as HTTPS, JWT/OAuth2, and RBAC, but I could improve it by doing a short threat model and showing diagrams of how login and sessions are handled. This would make the design stronger and easier for both the client and developers to understand.  

### Interpreting User Needs (and Why It Matters)  
I made sure to connect the software design to what the users would need during gameplay. For example, requiring unique names avoids confusion, and using WebSockets ensures fast, real-time updates, which are essential for a drawing game. Thinking about the user’s experience is key because even if the system works technically, it will not succeed if it does not feel smooth and enjoyable for the players (Mozilla, n.d.; IETF, 2011; IETF, 2015).  

### My Design Approach and Future Strategies  
My approach focused on using object-oriented design and multi-tier architecture to organize the system. Going forward, I would use more UML diagrams and Agile methods to improve my designs. I also want to include tools for observability such as metrics and logs so that the software can be monitored easily. These strategies would help me design applications that are more reliable and scalable in the future (PostgreSQL, n.d.; IETF, 2015).  

---

## References  

HAProxy. (n.d.). *Configuration and load balancing*. HAProxy. https://www.haproxy.com/documentation/haproxy-configuration/  

Internet Engineering Task Force (IETF). (2011). *The WebSocket protocol (RFC 6455)*. https://datatracker.ietf.org/doc/html/rfc6455  

Internet Engineering Task Force (IETF). (2012). *OAuth 2.0 authorization framework (RFC 6749)*. https://datatracker.ietf.org/doc/html/rfc6749  

Internet Engineering Task Force (IETF). (2015). *JSON Web Token (JWT) (RFC 7519)*. https://datatracker.ietf.org/doc/html/rfc7519  

Mozilla. (n.d.). *HTTP overview*. Mozilla Developer Network. https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview  

NGINX. (n.d.). *Load balancing overview*. NGINX Documentation. https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/  

Oracle. (n.d.). *Garbage-first (G1) garbage collector*. Oracle Documentation. https://docs.oracle.com/javase/8/docs/technotes/guides/vm/G1.html  

PostgreSQL. (n.d.). *Transactions and concurrency control*. PostgreSQL Documentation. https://www.postgresql.org/docs/current/transaction-iso.html  

Ubuntu. (n.d.-a). *LTS releases and support overview*. Ubuntu. https://ubuntu.com/about/release-cycle  

Ubuntu. (n.d.-b). *Ubuntu server*. Ubuntu. https://ubuntu.com/server  
