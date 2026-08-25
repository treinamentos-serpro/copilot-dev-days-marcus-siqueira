# Agent Instructions

## Mandatory development checklist

Before finishing any change, complete and report:

- [ ] Lint: run the applicable lint/static checks; this repository currently has no dedicated lint command.
- [ ] Build: `cd socops && ./mvnw clean package`
- [ ] Test: `cd socops && ./mvnw test`

Run the narrowest relevant check first, then the full checklist when shared
backend behavior changes.

## Project

Soc Ops is a social bingo game. The runnable Spring Boot app is under `socops/`
and listens on port 8080; `docs/` is the separately deployed static site. Run
Maven commands from `socops/` (see [README.pt_BR.md](README.pt_BR.md)).

## Architecture and rules

- [BingoRestController.java](socops/src/main/java/com/socops/web/BingoRestController.java) serves the page and fresh-board API.
- [BoardAssembler.java](socops/src/main/java/com/socops/service/BoardAssembler.java) is pure static domain logic; models and prompts are in `model/` and `data/`.
- [game.html](socops/src/main/resources/templates/game.html) owns Thymeleaf, vanilla JavaScript, and browser state (`localStorage` key `socops-bingo-snapshot`).
- Boards have 25 cells; slot 12 is a selected immutable free cell, with 24 prompts. Keep Java and JavaScript rules synchronized.
- Winning lines are checked in order: rows, columns, main diagonal, anti-diagonal. Domain changes require focused JUnit 5 tests in [BoardAssemblerTests.java](socops/src/test/java/com/socops/service/BoardAssemblerTests.java).

For frontend work, follow [CSS instructions](.github/instructions/css-utilities.instructions.md)
and [design instructions](.github/instructions/frontend-design.instructions.md); use
the existing Thymeleaf/vanilla CSS approach.

## References

Use the [workshop guide](workshop/pt_BR/GUIDE.md) for lab context. GitHub Pages
deploys [docs/index.html](docs/index.html); review [.github/workflows/deploy.yml](.github/workflows/deploy.yml)
before changing automation. Keep changes focused and preserve user changes.