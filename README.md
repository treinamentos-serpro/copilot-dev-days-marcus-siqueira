🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎱 Soc Ops

**The social bingo game that turns strangers into teammates.**

Find people who match the questions. Get 5 in a row. Break the ice — fast.

[![Java 21](https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-brightgreen?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-blue?logo=github)](https://treinamentos-serpro.github.io/copilot-dev-days-marcus-siqueira/)

</div>

---

## ✨ What is Soc Ops?

Soc Ops is a **live, in-browser Social Bingo** built for in-person developer events and workshops.
Each player gets a unique 5×5 board of icebreaker prompts. Walk around, chat with people, and mark off cells when you find a match — first to fill a row, column, or diagonal wins!

The app is also a **hands-on GitHub Copilot workshop** — you'll build new features, design the frontend, and craft custom AI agents, all guided by the lab exercises below.

---

## 🚀 Quick Start

> **Prerequisites:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) (or use the included wrapper)

```bash
git clone https://github.com/treinamentos-serpro/copilot-dev-days-marcus-siqueira.git
cd copilot-dev-days-marcus-siqueira/socops
./mvnw spring-boot:run
```

Open [http://localhost:8080](http://localhost:8080) and start playing. 🎉

---

## 🗺️ Lab Guide

Work through the exercises in order to build and extend Soc Ops with GitHub Copilot:

| # | Lab | What you'll build |
|---|-----|-------------------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | Orient yourself and verify your setup |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | Configure Copilot context for the project |
| [**02**](workshop/02-design.md) | Design-First Frontend | Redesign the game UI from scratch |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | Create a custom Copilot agent for content |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | Orchestrate agents to ship a full feature |

📚 Full guide: **[workshop/GUIDE.md](workshop/GUIDE.md)**

---

## 🏗️ Project Structure

```
socops/          Spring Boot app (port 8080)
├── src/main/
│   ├── java/    Domain logic & REST controller
│   └── resources/templates/   game.html (Thymeleaf + vanilla JS)
workshop/        Step-by-step lab exercises
docs/            Static site deployed to GitHub Pages
```

---

## 🛠️ Common Commands

| Task | Command |
|------|---------|
| Run locally | `cd socops && ./mvnw spring-boot:run` |
| Build JAR | `cd socops && ./mvnw clean package` |
| Run tests | `cd socops && ./mvnw test` |

Pushes to `main` deploy automatically to **GitHub Pages**.
