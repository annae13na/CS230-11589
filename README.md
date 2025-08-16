# CS230-11589
M01 Operating Platforms 2025
# CS 230 – Module Eight Journal: Portfolio Reflection

## Artifact Submitted
**Artifact:** Completed Software Design Document for *Draw It or Lose It – Web Version*  
**Client:** The Gaming Room  
**Repo Location:** `docs/CS230-Software-Design-Document.pdf` (update this path to match your repo)

---

## Reflection

### 1) Client & Software Requirements
The Gaming Room requested a **web-based, cross-platform** version of its Android game *Draw It or Lose It*. Key requirements included supporting multiple teams and players, enforcing **unique game and team names**, maintaining **only one instance** of the game service in memory (Singleton), and ensuring scalable performance and secure networked communication suitable for distributed use.

### 2) What I Did Well
I translated client requirements into a clear **object-oriented domain model**, using an `Entity` base class (for Game, Team, Player) with encapsulation and consistent identifiers. I applied the **Singleton** pattern for `GameService` to centralize state and the **Iterator/search** approach to enforce unique names efficiently. My platform evaluation and recommendations balanced **cost, maintainability, and scalability**, aligning choices like Ubuntu Server LTS, PostgreSQL, and containerization with real-world operations [1][2][3].

### 3) How the Design Document Helped the Code
Working through the design document forced me to **plan before building**: clarifying constraints, picking deployment targets, and defining memory/storage approaches. That upfront analysis streamlined coding and reduced rework, because the architectural decisions (e.g., a multi-tier design with REST + optional WebSockets for realtime play) were already justified against requirements [4][5][6].

### 4) What I Would Revise (and How)
I would expand the **security section** with a brief **threat model**, detailing risks (injection, auth/session abuse, misuse of realtime channels) and mapping them to mitigations (input validation, parameterized queries, JWT/OAuth2 with RBAC, HTTPS, key rotation, security headers, rate-limiting) with a small **sequence diagram** for auth/token refresh. I would also add **operational runbooks** (e.g., backup/restore steps, incident response) and SLOs to tighten reliability.

### 5) Interpreting User Needs in the Design (and Why It Matters)
User needs drove choices like **unique names** (avoid confusion in multiplayer lobbies), **low-latency updates** for drawing/guessing (WebSockets), and **scalable session handling** (stateless REST + token-based auth). Designing from user needs ensures the product is **usable, performant, and trustworthy**, which directly impacts engagement and retention [4][5][7].

### 6) My Design Approach & Go-Forward Strategies
I combined **OO design**, **design patterns**, and a **multi-tier architecture** (presentation, application, data). In future projects, I’ll:
- Prototype early, then iterate with **Agile feedback** cycles.
- Use **UML** (class, sequence, deployment) to surface integration risks early.
- Employ **containerization** and IaC for consistent environments and easy scaling.
- Tune the JVM with **G1GC** targets for predictable latency under load [3].
- Add **observability** (metrics, tracing, logs) and automated security checks in CI/CD.

---

## Quick Rationale for Key Technical Choices (with Sources)
- **Ubuntu Server LTS** for cost-effective, secure, and long-term supported deployments [1][2].  
- **PostgreSQL** for relational, ACID-compliant storage and strong concurrency control [6].  
- **G1 Garbage Collector** for low-pause, predictable performance in server-side Java [3].  
- **REST over HTTPS** plus **WebSockets** for realtime gameplay (I/O efficient, standardized) [4][5].  
- **OAuth 2.0/JWT** for interoperable, stateless authentication and session management [7][8].  
- **NGINX/HAProxy** for load-balancing and horizontal scalability [9][10].

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

---

## How to View This Artifact
- Open the design document at `docs/CS230-Software-Design-Document.pdf`.
- This README section serves as the **Module Eight Journal** reflection for the portfolio.
