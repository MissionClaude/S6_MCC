# claude-ci-cd-app

Aplicación Angular "Hola Mundo" usada como base para practicar el flujo de CI/CD con Claude Code (GitHub Actions).

## Comandos

- `npm start` — servidor de desarrollo (`ng serve`)
- `npm run build` — build de producción
- `npm run lint` — ESLint (`@angular-eslint`)
- `npm test` — tests unitarios en modo watch (Karma + Jasmine)
- `npm run test:ci` — tests unitarios headless con cobertura, usado en CI

## CI/CD

- `.github/workflows/ci.yml` — lint, test y build en cada push/PR a `main`.
- `.github/workflows/claude.yml` — permite invocar a Claude Code respondiendo `@claude` en issues, PRs o comentarios.
- `.github/workflows/claude-code-review.yml` — Claude revisa automáticamente cada PR abierto o actualizado.

Los workflows de Claude requieren el secret `ANTHROPIC_API_KEY` configurado en el repositorio de GitHub (Settings → Secrets and variables → Actions).
