# CS230-11589
M01 Operating Platforms 2025
# CS 230 – Module Eight Journal: Portfolio Reflection

---

## Reflection

### 1) Client & Software Requirements
The Gaming Room is a company that wanted to expand its Android game *Draw It or Lose It* into a **web-based, cross-platform version**. The software needed to support multiple teams and players, make sure that names were unique, and use only **one instance of the game service** in memory (through the Singleton pattern). The client also wanted the game to be scalable, secure, and able to run smoothly across different devices.

### 2) What I Did Well
I think I did well in creating a **clear design structure** that matched the client’s needs. I built a domain model that used inheritance and encapsulation to avoid duplicate code, and I applied design patterns like **Singleton** and **Iterator** to keep the system efficient. I also feel confident about my platform recommendations, such as choosing Ubuntu Server LTS and PostgreSQL, because they balance cost, reliability, and scalability [1][2][3].

### 3) How the Design Document Helped the Code
Writing the design document first really helped me when it came time to think about coding. It made me slow down and plan instead of just jumping in. By laying out things like memory management, storage, and system layers, I already had answers to a lot of problems before I started building. For example, knowing I would use REST APIs and possibly WebSockets gave me a roadmap for how communication would work between players [4][5][6].

### 4) What I Would Revise (and How)
If I could revise one part of my design document, I would add more detail to the **security section**. I mentioned things like HTTPS, JWT/OAuth2, and RBAC, but I could improve it by doing a short **threat model** and showing diagrams of how login and sessions are handled. I think this would make the design stronger and easier for both the client and developers to understand.

### 5) Interpreting User Needs (and Why It Matters)
I made sure to connect the software design to what the users would need during gameplay. For example, requiring unique names avoids confusion, and using WebSockets ensures fast, real-time updates, which are very important for a drawing game. Thinking about the user’s experience is key because even if the system works technically, it won’t succeed if it doesn’t feel good for the players [4][5][7].

### 6) My Design Approach & Future Strategies
My approach focused on using **object-oriented design** and **multi-tier architecture** to organize the system. Going forward, I would use more **UML diagrams** and **Agile methods** to improve my designs. I also want to include tools for **observability** like metrics and logs so that the software can be monitored easily. These strategies would help me design applications that are more reliable and scalable in the future [3][6][8].

---

## Key Technical Choices (with Sources)
- **Ubuntu Server LTS** for stability, cost savings, and long-term support [1][2].  
- **PostgreSQL** for ACID-compliant storage and strong concurrency [6].  
- **G1 Garbage Collector** in the JVM for predictable performance [3].  
- **REST over HTTPS** plus **WebSockets** for communication and real-time play [4][5].  
- **OAuth2 and JWT** for secure authentication and session management [7][8].  
- **NGINX/HAProxy** for load balancing and scaling [9][10].

---

## References
[1] Ubuntu – LTS releases and support overview: https://ubuntu.com/about/release-cycle  
[2] Ubuntu Server – Official docs: https://ubuntu.com/server  
[3] Oracle Docs – Garbage-First (G1) Garbage Collector: https://docs.oracle.com/javase/8/docs/technotes/guides/vm/G1.html  
[4] Mozilla MDN – HTTP Overview (REST over HTTPS fundamentals): https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview  
[5] RFC 6455 – The WebSocket Protocol (IETF): https://datatracker.ietf.org/doc/html/rfc6455  
[6] PostgreSQL Docs – Transactions & Concurrency (ACID): https://www.postgresql.org/docs/current/transaction-iso.html  
[7] OAuth 2.0 – RFC 6749 (IETF): https://datatracker.ietf.org/doc/html/rfc6749  
[8] JSON Web Token (JWT) – RFC 7519 (IETF): https://datatracker.ietf.org/doc/html/rfc7519  
[9] NGINX – Load Balancing Overview: https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/  
[10] HAProxy – Configuration & Load Balancing: https://www.haproxy.com/documentation/haproxy-configuration/

