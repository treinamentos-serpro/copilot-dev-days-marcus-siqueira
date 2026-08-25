<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎱 Soc Ops

**El juego de bingo social que convierte desconocidos en compañeros de equipo.**

Encuentra personas que coincidan con las preguntas. Consigue 5 en línea. Rompe el hielo — rápido.

[![Java 21](https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-brightgreen?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![GitHub Pages](https://img.shields.io/badge/Desplegado-GitHub%20Pages-blue?logo=github)](https://treinamentos-serpro.github.io/copilot-dev-days-marcus-siqueira/)

</div>

---

## ✨ ¿Qué es Soc Ops?

Soc Ops es un **Social Bingo en vivo, directo en el navegador**, creado para eventos presenciales y talleres de desarrollo.
Cada jugador recibe un tablero 5×5 único con preguntas para romper el hielo. Circula por el evento, conversa con las personas y marca las celdas cuando encuentres una coincidencia — ¡el primero en completar una fila, columna o diagonal gana!

La app es también un **taller práctico de GitHub Copilot** — crearás nuevas funcionalidades, diseñarás el frontend y elaborarás agentes de IA personalizados, guiado por los ejercicios de laboratorio a continuación.

---

## 🚀 Inicio Rápido

> **Requisitos previos:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) (o usa el wrapper incluido)

```bash
git clone https://github.com/treinamentos-serpro/copilot-dev-days-marcus-siqueira.git
cd copilot-dev-days-marcus-siqueira/socops
./mvnw spring-boot:run
```

Abre [http://localhost:8080](http://localhost:8080) y empieza a jugar. 🎉

---

## 🗺️ Guía del Lab

Sigue los ejercicios en orden para construir y ampliar Soc Ops con GitHub Copilot:

| # | Lab | Qué vas a construir |
|---|-----|---------------------|
| [**00**](workshop/es/00-overview.md) | Descripción General y Lista de Verificación | Oriéntate y verifica tu entorno |
| [**01**](workshop/es/01-setup.md) | Configuración e Ingeniería de Contexto | Configura el contexto de Copilot para el proyecto |
| [**02**](workshop/es/02-design.md) | Desarrollo Frontend Orientado al Diseño | Rediseña la interfaz del juego desde cero |
| [**03**](workshop/es/03-quiz-master.md) | Quiz Master Personalizado | Crea un agente Copilot personalizado para contenido |
| [**04**](workshop/es/04-multi-agent.md) | Desarrollo Multi-Agente | Orquesta agentes para entregar una funcionalidad completa |

📚 Guía completa: **[workshop/es/GUIDE.md](workshop/es/GUIDE.md)**

---

## 🏗️ Estructura del Proyecto

```
socops/          Aplicación Spring Boot (puerto 8080)
├── src/main/
│   ├── java/    Lógica de dominio y controlador REST
│   └── resources/templates/   game.html (Thymeleaf + vanilla JS)
workshop/        Ejercicios paso a paso del lab
docs/            Sitio estático desplegado en GitHub Pages
```

---

## 🛠️ Comandos Comunes

| Tarea | Comando |
|-------|---------|
| Ejecutar localmente | `cd socops && ./mvnw spring-boot:run` |
| Generar JAR | `cd socops && ./mvnw clean package` |
| Ejecutar pruebas | `cd socops && ./mvnw test` |

Los push a `main` se despliegan automáticamente en **GitHub Pages**.
