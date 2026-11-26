# Stack e arquitetura

| Camada | Escolha | Observação |
| --- | --- | --- |
| Front-end | Angular 22 (standalone, rotas, formulários reativos) | Cada tela do protótipo vira uma rota |
| Estilo | Tailwind CSS 4 | Tokens em variáveis CSS; `darkMode` por classe |
| Design System | GovDS + Design System do CPAT | Biblioteca interna de componentes |
| API simulada (v1) | JSON Server | Troca por API real na v2 |
| Servidor web | Nginx em container Docker | Fallback de rotas, gzip e cabeçalhos de segurança |
| Chat | JivoChat | Exige o ID da conta do CPAT |
| Testes | Vitest (unitários) e Playwright (e2e) | Com axe para acessibilidade |
| CI/CD | GitHub Actions | Lint, build, links e testes por pull request |
| Back-end e banco (v2) | Hipótese: Ruby on Rails e PostgreSQL | Fora da v1 |

## Fluxo de dados na v1

```
Angular (serviço de dados) → /api (proxy) → JSON Server → db.json
```

Os dados passam por serviços Angular com interfaces tipadas; trocar o JSON Server por uma API real não exige refazer as telas.
