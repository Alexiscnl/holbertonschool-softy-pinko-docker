# 🚀 Softy Pinko Docker Project

![Docker Banner](https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png)

---

## 🌟 Context

> **Docker** is a platform that allows you to containerize your applications, making them portable and easy to run anywhere. Move your app from your laptop to a server without worrying about dependencies or configuration issues!

Containers are:

- 🧳 Self-contained
- ⚡ Lightweight & fast
- 🔄 Easy to scale
- 🛠️ Managed with orchestration tools like Docker Compose

---

## 🏗️ Project Overview

In this project, you will build an infrastructure with:

| Component        | Description                |
| ---------------- | -------------------------- |
| 🔀 Reverse Proxy | Routes traffic to services |
| ⚖️ Load Balancer | Distributes API requests   |
| 🖥️ API Servers   | Two application servers    |
| 🎨 Front-end     | Static-content server      |

---

## 🖼️ High-level Design

The entry point is a single server acting as:

- 🔀 **Reverse Proxy**: Routes traffic to API or front-end
- ⚖️ **Load Balancer**: Balances traffic between API servers (Round Robin)

### 🔄 Traffic Flow

**Front-end Requests**

> Routed to the front-end static-content server. Static content is returned to the proxy, then sent to the client. The client never talks directly to the front-end server.

**API Requests**

> Routed through a load-balancing algorithm (Round Robin) to one of the API servers. Response goes back to the proxy, then to the client. The client never talks directly to the API servers.

---

## ⚡ What is Round Robin Load Balancing?

Round Robin distributes traffic across servers in a rotating manner:

| Request | Server |
| ------- | ------ |
| 1       | A      |
| 2       | B      |
| 3       | C      |
| 4       | A      |
| ...     | ...    |

✅ Ensures equal share of traffic
✅ Prevents overload
❗ Simple & effective for learning purposes

---

## 📝 Prerequisites

- 🖥️ Install Docker Desktop: [Docker Download](https://www.docker.com/)
- 📚 Installation guides:
  - [Windows](https://docs.docker.com/desktop/install/windows-install/)
  - [Mac](https://docs.docker.com/desktop/install/mac-install/)
  - [Linux](https://docs.docker.com/desktop/install/linux-install/)
  - Chromebook: Docker engine only, not Desktop (compatibility may vary)
- 🎓 Learn Docker: [Docker Tutorial](https://docs.docker.com/get-started/)

---

## 📚 Useful Resources

- [Docker Cheatsheet](https://dockerlabs.github.io/docker-cheat-sheet/)
- [Proxy vs Reverse Proxy (Real-world Examples)](https://www.imperva.com/learn/application-security/reverse-proxy/)
- [What is a Reverse Proxy? (vs. Forward Proxy) | Proxy servers explained](https://www.youtube.com/watch?v=7QmCUDHpNzE) _(Stop at 06:25)_

---

> **Ready to containerize and scale? Let’s go! 🐳**
