# Testes

| Tipo | Ferramenta | Escopo |
| --- | --- | --- |
| Unitários | Vitest | Serviços (vagas, tema, fonte) e componentes base |
| E2E | Playwright | Filtrar vagas, modal da vaga, modo escuro, A−/A+, teclado, SAC simulado |
| Acessibilidade | axe e Lighthouse | Toda entrega; `@axe-core/playwright` nos e2e |
| Links | Verificador de links | A cada build e semanalmente |

Os testes rodam no CI a cada pull request.
