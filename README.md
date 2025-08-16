# CS230-11589
M01 Operating Platforms 2025
# 🎮 CS 230 Module Eight Journal – Portfolio Reflection

## The Gaming Room: Client and Software Requirements

**Client:** The Gaming Room  
**Existing Product:** *Draw It or Lose It* (Android)  
**Goal:** Expand to a web-based, cross-platform application.

**Core needs:**  
- Multiple simultaneous games with multiple teams and players  
- Enforcing **unique game and team names**  
- Only one instance of the game service in memory (**Singleton pattern**)  
- A **distributed system** that allows communication across platforms  
- **Secure** handling of user authentication and data

---

## ✅ What I Did Well

I connected the client’s requirements to concrete technical solutions. Highlights include:

- Using **object-oriented design** and patterns like **Singleton** and **Iterator** to help ensure unique naming and efficient memory use.  
- Recommending a **Linux-based server environment** for scalability, cost savings, and stability.  
- Explaining **memory vs. storage** management with real application needs in mind (fast image rendering and large image library storage).

---

## 🧩 Helpful Parts of the Design Process

The software design document process helped me think ahead before writing code. Instead of coding first, I planned around:

- **Memory management:** fast rendering of 200+ high‑resolution images so gameplay stayed smooth.  
- **Storage needs:** organizing large image files and user data.  
- **Distributed systems:** ensuring players on different devices could connect seamlessly.

That preparation made implementing **authentication** and **REST APIs** easier later because scalability and security were already considered.

---

## 🔁 What I Would Revise

If I could revise one section, it would be the **Distributed Systems and Networks** explanation. I covered scalability, but I would go deeper into:

- **Real-time communication** options (e.g., **WebSockets**)  
- **Fault tolerance and failover** strategies

This would better show the client how the game could remain stable during outages and spikes.

---

## 🔎 Interpreting and Implementing User Needs

I carefully mapped user needs into technical features:

- **Unique game/team names** → Implemented with **Iterator** pattern and collection checks.  
- **Single game instance** → Enforced with the **Singleton** pattern.  
- **Fast rendering performance** → Optimized memory handling for images.  
- **Security** → Used **REST API** with authentication and role-based access.

Considering user needs is critical because even the best technical design fails if it doesn’t align with user experience and client expectations.

---

## 🧠 Memory vs. 💾 Storage Management

In this project, I learned how memory and storage management work together but serve different purposes:

- **Memory management** focuses on short-term performance. For example, *Draw It or Lose It* needed to load and display ~8 MB images rapidly during gameplay, which meant efficient allocation and garbage collection in memory.  
- **Storage management** ensures long-term data organization. The game required permanent storage for its large library of images and player records, so a database or file system had to manage that efficiently.

**In short:** *Memory enables speed*, while *storage provides capacity*—both are essential for balancing performance and reliability.

---

## 🏗️ My Approach to Designing Software

- **Client–server architecture** with **REST APIs**  
- **Design patterns** (Singleton, Iterator) for efficiency  
- **Secure authentication** with **Dropwizard** (BasicAuth + role-based access)  
- **Cross-platform evaluation** of Linux, Windows, macOS, Android, and iOS

**Future enhancements:**  
- Leverage **cloud-native** tools (containers, auto-scaling, load balancing)  
- Build **security by design** (encryption, stronger auth than BasicAuth)  
- Use **architecture diagrams** and **UML** to communicate designs more effectively

---

## 🗂️ References 

- Oracle. (2024). *Memory management in the Java HotSpot™ virtual machine*. https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/  
- Red Hat. (2023). *Introduction to Linux operating system*. https://www.redhat.com/en/topics/linux/what-is-linux  
- OWASP Foundation. (2023). *Authentication cheat sheet*. https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html  
- GeeksforGeeks. (2024). *Difference between memory management and storage management*. https://www.geeksforgeeks.org/difference-between-memory-management-and-storage-management/

---

> 📌 *This journal reflection is part of my portfolio submission for CS 250 and showcases my ability to design, analyze, and reflect on software development for a real‑world client scenario.*
