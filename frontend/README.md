# Frontend — CPAT Campinas

Interface do usuário do site do CPAT. v1 só com front-end: **Angular 22** (componentes standalone, SSR com pré-renderização) e **Tailwind CSS 4**, seguindo o Gov.br Design System e o Design System do CPAT. Ver [docs/briefing.md](../docs/briefing.md).

## Requisitos

- Node.js 22 ou superior
- npm 10 ou superior

## Como rodar

```bash
cd frontend
npm install
npm start          # http://localhost:4200
```

## Scripts

| Comando | O que faz |
| --- | --- |
| `npm start` | Servidor de desenvolvimento |
| `npm run build` | Build de produção, com SSR e pré-renderização das rotas |
| `npm test` | Testes unitários (Vitest) |
| `npm run lint` | ESLint (angular-eslint) |
| `npm run serve:ssr:cpat-frontend` | Serve o build com SSR (depois do `build`) |

## Estrutura

```
src/
├── styles.css          # Tailwind e tokens (claro/escuro) do GovDS e do CPAT
└── app/
    ├── app.*           # Shell: link "ir para o conteúdo", cabeçalho e rota
    └── pages/home/     # Home provisória
```

## Tokens e tema

Os tokens estão em `src/styles.css`, em variáveis CSS ligadas ao tema do Tailwind (`bg-primaria`, `text-texto`, `border-borda-campo`, `max-w-pagina` etc.). O modo escuro funciona pela classe `dark` no `<html>`. O tamanho da fonte A−/A+ muda `--cpat-fonte-base`, e as medidas em `rem` acompanham.

## Próximos passos

Acompanhe as [issues](https://github.com/Paul0Ant0ni0/cpat-digital/issues) do projeto.
