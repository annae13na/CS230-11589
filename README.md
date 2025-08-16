# CS250-12670
M01 Software Development Lifecycle 2025
# 🎮 CS 250 Module Eight Journal – Reflection

## 1. Briefly summarize The Gaming Room client and their software requirements
The client, **The Gaming Room**, wanted to expand their Android game *Draw It or Lose It* into a web-based application that could support multiple platforms. Their main requirements included:
- Supporting multiple teams and players  
- Ensuring game and team names are unique  
- Limiting the system to a single game service instance in memory  
- Making the system scalable and secure across platforms  

---

## 2. What did you do particularly well in developing this documentation?
I did particularly well in explaining the **system architecture** and making clear recommendations for the **operating platform, storage management, and security**. I also clearly connected the client’s needs to technical solutions, such as using the **Singleton design pattern** for memory efficiency.

---

## 3. What about the process of working through a design document did you find helpful when developing the code?
The process helped me think through **design decisions before coding**. By outlining requirements, constraints, and architecture early, I could identify potential challenges (like distributed communication or securing user data) before writing any actual code. This made the coding process more **organized and efficient**.

---

## 4. If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?
If I could revise one part, I would improve the **Distributed Systems** section. I originally gave a high-level explanation, but I would expand it with more detail about:
- Real-time communication (e.g., WebSockets)  
- Specific examples of **failover strategies**  

That would make the design more complete and practical.

---

## 5. How did you interpret the user’s needs and implement them into your software design? Why is it so important to consider the user’s needs when designing?
I interpreted the user’s needs by carefully analyzing the requirements:
- Only one game service instance should run (Singleton pattern)  
- Unique team and game names must be enforced  
- The application must scale across multiple platforms  

It’s important to consider the user’s needs because software should **solve the client’s actual problem**, not just be technically correct. If the design doesn’t reflect what the client wants, the final product won’t meet expectations.

---

## 6. How did you approach designing software? What techniques or strategies would you use in the future to analyze and design a similar software application?
I approached the design using:
- **Object-Oriented Programming (OOP)** principles  
- **Design patterns** like Singleton and Iterator  
- **Multi-tier architecture** strategies  

In the future, I would continue these practices but also place more emphasis on:  
- **Security by design**  
- **Cloud-native features** (like auto-scaling and containerization)  
- Using diagrams (UML, architecture diagrams) to make the design easier to communicate  

---

📌 *This journal reflection is part of my portfolio submission for CS 230.*
