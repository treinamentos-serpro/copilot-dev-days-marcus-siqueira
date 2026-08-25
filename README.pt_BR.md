<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎱 Soc Ops

**O jogo de bingo social que transforma desconhecidos em parceiros de time.**

Encontre pessoas que correspondam às perguntas. Faça 5 em linha. Quebre o gelo — rápido.

[![Java 21](https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-brightgreen?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![GitHub Pages](https://img.shields.io/badge/Implantado-GitHub%20Pages-blue?logo=github)](https://treinamentos-serpro.github.io/copilot-dev-days-marcus-siqueira/)

</div>

---

## ✨ O que é o Soc Ops?

Soc Ops é um **Social Bingo ao vivo, direto no navegador**, feito para eventos presenciais e workshops de desenvolvimento.
Cada jogador recebe um tabuleiro 5×5 único com perguntas para quebrar o gelo. Circule pelo evento, converse com as pessoas e marque as células quando encontrar uma correspondência — quem completar uma linha, coluna ou diagonal primeiro ganha!

O app é também um **workshop prático de GitHub Copilot** — você vai construir novas funcionalidades, criar o frontend e elaborar agentes de IA personalizados, guiado pelos exercícios de laboratório abaixo.

---

## 🚀 Início Rápido

> **Pré-requisitos:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) (ou use o wrapper incluído)

```bash
git clone https://github.com/treinamentos-serpro/copilot-dev-days-marcus-siqueira.git
cd copilot-dev-days-marcus-siqueira/socops
./mvnw spring-boot:run
```

Abra [http://localhost:8080](http://localhost:8080) e comece a jogar. 🎉

---

## 🗺️ Guia do Lab

Siga os exercícios em ordem para construir e evoluir o Soc Ops com o GitHub Copilot:

| # | Lab | O que você vai construir |
|---|-----|--------------------------|
| [**00**](workshop/pt_BR/00-overview.md) | Visão Geral & Lista Rápida | Oriente-se e verifique o ambiente |
| [**01**](workshop/pt_BR/01-setup.md) | Configuração & Engenharia de Contexto | Configure o contexto do Copilot para o projeto |
| [**02**](workshop/pt_BR/02-design.md) | Frontend Design-First | Redesenhe a interface do jogo do zero |
| [**03**](workshop/pt_BR/03-quiz-master.md) | Quiz Master Personalizado | Crie um agente Copilot customizado para conteúdo |
| [**04**](workshop/pt_BR/04-multi-agent.md) | Desenvolvimento Multi-Agente | Orquestre agentes para entregar uma feature completa |

📚 Guia completo: **[workshop/pt_BR/GUIDE.md](workshop/pt_BR/GUIDE.md)**

---

## 🏗️ Estrutura do Projeto

```
socops/          Aplicação Spring Boot (porta 8080)
├── src/main/
│   ├── java/    Lógica de domínio & controlador REST
│   └── resources/templates/   game.html (Thymeleaf + vanilla JS)
workshop/        Exercícios passo a passo do lab
docs/            Site estático implantado no GitHub Pages
```

---

## 🛠️ Comandos Comuns

| Tarefa | Comando |
|--------|---------|
| Executar localmente | `cd socops && ./mvnw spring-boot:run` |
| Gerar JAR | `cd socops && ./mvnw clean package` |
| Rodar testes | `cd socops && ./mvnw test` |

Pushes para `main` fazem deploy automático no **GitHub Pages**.
